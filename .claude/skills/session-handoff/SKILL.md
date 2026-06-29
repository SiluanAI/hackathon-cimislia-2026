---
name: session-handoff
description: >-
  Scrie un rezumat de predare a sesiunii ÎNAINTE de a face /clear sau de a
  porni o sesiune nouă, ca să continui exact de unde ai rămas fără să pierzi
  context. Folosește când conversația s-a umflat (Claude devine lent/uită), când
  vrei să eviti "context rot", sau când muți munca în altă sesiune/alt model.
  Produce un bloc gata de copiat: ce s-a făcut, fișiere cheie, decizii, stare
  git, întrebări deschise și unde reiei.
---

# Session Handoff

Conversațiile lungi degradează calitatea (context rot): Claude devine mai lent,
uită, halucinează — cu mult înainte ca fereastra de context să fie plină. Soluția
nu e `/compact` (lent, pierde nuanțe), ci o **predare curată**: rezumi ce contează,
faci `/clear`, lipești rezumatul → fereastră curată, dar continui exact de unde erai.

**Când o rulezi:**
- Când fereastra de context trece de ~25% (vezi `/context`) sau Claude începe să uite.
- Înainte de `/clear`.
- Când muți munca în altă sesiune sau alt model (Codex etc.).
- La finalul unei sesiuni de lucru, ca punct de reluare pentru data viitoare.

---

## Pasul 1 — Asigură persistența (mediul e efemer)

Containerul se șterge după inactivitate. Înainte de handoff, verifică rapid:
- Decizii importante logate în `decisions/log.md`? Dacă nu, loghează-le acum.
- Modificări necomise? Spune-i utilizatorului ce e necomis/nepush-uit. Un handoff
  fără commit/push nu salvează munca, doar contextul.

---

## Pasul 2 — Scrie blocul de handoff

Produ EXACT structura de mai jos, în română cu diacritice, într-un singur bloc
de cod ușor de copiat. Fii concret și scurt — fără umplutură. Dacă o secțiune e
goală, scrie "—", n-o inventa.

```
═══════════════ SESSION HANDOFF ═══════════════
Data: <YYYY-MM-DD HH:MM>  ·  Branch: <branch>  ·  Repo: Liron YouTube

DE UNDE AM PORNIT (obiectivul sesiunii):
<1-2 rânduri — ce am vrut să rezolvăm>

CE S-A LIVRAT:
- <rezultat concret 1>
- <rezultat concret 2>

DECIZII BLOCATE (nu le redeschide fără motiv):
- <decizie + de ce>

FIȘIERE CHEIE (unde să te uiți):
- `cale/fișier` — <ce conține / de ce contează>

STARE GIT:
- Branch: <branch> · Ultim commit: <hash + mesaj scurt>
- Necomis: <da/nu — ce> · Push-uit: <da/nu>

VERIFICAT (ce e confirmat că merge vs neconfirmat):
- <ce am testat și a trecut> / <ce NU e încă verificat>

AMÂNAT / ÎNTREBĂRI DESCHISE:
- <fir deschis 1 — ce decizie aștaptă de la Sil>

REIA DE AICI (primul pas concret în sesiunea nouă):
1. <acțiunea exactă următoare>
═══════════════════════════════════════════════
```

---

## Pasul 3 — Instrucțiuni de reluare

După bloc, spune-i utilizatorului exact ce să facă:

1. `/copy` (sau copiază manual blocul de mai sus).
2. `/clear` — golește fereastra de context.
3. Lipește blocul ca primul mesaj în sesiunea curată.

În sesiunea nouă, Claude citește mai întâi `CLAUDE.md` (Step 0: `git pull` +
strategia), apoi blocul de handoff îi dă starea exactă — și continuă din "REIA
DE AICI".

---

## Note

- Handoff-ul rezumă CONTEXTUL, nu salvează FIȘIERELE. Persistența reală =
  commit + push (vezi Pasul 1).
- Nu pune secrete/chei în bloc — ajunge în istoricul conversației.
- Ține-l scurt: scopul e o fereastră curată, nu să recreezi toată conversația.
