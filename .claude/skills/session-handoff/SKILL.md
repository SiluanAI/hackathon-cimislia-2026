---
name: session-handoff
description: >-
  Scrie un rezumat de predare a sesiunii ca să continui exact de unde ai rămas
  fără să pierzi context. Rulează OBLIGATORIU când contextul trece de 225.000
  tokeni (plafon dur 250k, niciodată depășit), înainte de /clear, sau când muți
  munca în altă sesiune. Salvează handoff-ul ca fișier comis în
  decisions/handoffs/ (durabil, supraviețuiește containerului efemer) și opțional
  ca bloc de copiat pentru /clear rapid.
---

# Session Handoff

Conversațiile lungi degradează calitatea (context rot): Claude devine lent, uită,
halucinează — cu mult înainte ca fereastra să fie plină. Soluția: o **predare
curată** într-un fișier comis, ca o sesiune nouă să continue exact de unde erai.

## Pragul de tokeni (regulă fermă)

- La **225.000 tokeni** (vezi `/context` sau statusline) → rulează ACEST skill imediat.
- **250.000 tokeni = plafon dur. Niciodată depășit.** Dacă te apropii, oprește orice
  altceva și fă handoff-ul + `/clear`.
- Alte momente: înainte de `/clear`, la mutarea muncii în altă sesiune/model, la
  finalul unei sesiuni de lucru.

---

## Pasul 1 — Asigură persistența (mediul e efemer)

Containerul se șterge după inactivitate. Înainte de handoff:
- Decizii importante logate în `decisions/log.md`? Dacă nu, loghează-le acum.
- Modificări necomise/nepush-uite? Spune-i utilizatorului. **Handoff-ul salvează
  CONTEXTUL, nu FIȘIERELE** — persistența reală = commit + push.

---

## Pasul 2 — Scrie handoff-ul ca fișier comis (calea durabilă)

Creează fișierul:
```
decisions/handoffs/YYYY-MM-DD-HHMM-<topic-slug>.md
```
- `topic-slug` = topicul principal al sesiunii, scurt, cu liniuțe (ex:
  `pret-site-programare`, `skill-council`, `pachet-video-07`).
- Prefixul dată-oră face fișierele să se sorteze cronologic singure → cel mai
  recent e mereu ultimul la listare.

Conținutul fișierului (română cu diacritice, concret, fără umplutură; secțiune
goală = "—"):

```
═══════════════ SESSION HANDOFF ═══════════════
Data: <YYYY-MM-DD HH:MM>  ·  Topic: <topicul principal>
Branch: <branch>  ·  Repo: Liron YouTube  ·  Status: <ACTIV | ÎNCHIS>

DE UNDE AM PORNIT (obiectivul sesiunii):
<1-2 rânduri>

CE S-A LIVRAT:
- <rezultat concret>

DECIZII BLOCATE (nu le redeschide fără motiv):
- <decizie + de ce>

FIȘIERE CHEIE (unde să te uiți):
- `cale/fișier` — <ce conține / de ce contează>

STARE GIT:
- Branch: <branch> · Ultim commit: <hash + mesaj scurt>
- Necomis: <da/nu — ce> · Push-uit: <da/nu>

VERIFICAT (confirmat că merge vs neconfirmat):
- <ce a trecut> / <ce NU e încă verificat>

AMÂNAT / ÎNTREBĂRI DESCHISE:
- <fir deschis — ce decizie așteaptă de la Sil>

REIA DE AICI (primul pas concret în sesiunea nouă):
1. <acțiunea exactă următoare>
═══════════════════════════════════════════════
```

Pune `Status: ÎNCHIS` când firul e terminat (ca să nu fie reluat din greșeală);
`ACTIV` dacă rămâne treabă pe el.

Comite fișierul: `git add decisions/handoffs/<fișier> && git commit` (și push dacă
se poate). Așa supraviețuiește morții containerului.

---

## Pasul 3 — Opțional: bloc de copiat pentru /clear rapid

Dacă vrei doar să cureți fereastra în ACEEAȘI sesiune (containerul trăiește),
afișează și conținutul ca bloc, apoi: `/copy` → `/clear` → lipești blocul.
Pentru "închid laptopul și revin mâine", fișierul comis (Pasul 2) e suficient —
nu depinde de clipboard.

---

## Cum continuă sesiunea NOUĂ (citește asta la pornire)

1. `git pull` (vezi `CLAUDE.md` Step 0).
2. Listează `decisions/handoffs/` — fișierele se sortează cronologic.
3. **Implicit: citește cel mai RECENT fișier cu `Status: ACTIV`** și continuă din
   secțiunea "REIA DE AICI".
4. Dacă există mai multe fire ACTIVE, sau utilizatorul a numit un topic anume,
   citește fișierul cu acel topic în nume. Dacă e ambiguu, enumeră firele active
   (dată + topic) și întreabă pe care îl reia.

---

## Note

- Nu pune secrete/chei în handoff — ajunge în git.
- Ține-l scurt: scopul e o fereastră curată, nu re-crearea conversației.
- Handoff-urile vechi rămân ca istoric; marchează-le `ÎNCHIS` când termini firul.
