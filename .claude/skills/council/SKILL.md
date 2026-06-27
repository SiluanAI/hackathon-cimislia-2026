---
name: council
description: >-
  Stress-testează o DECIZIE cu economics reale (preț, ofertă, pivot, idee de
  produs/business) cu un consiliu adversarial înainte de a investi timp. Scopul
  e să scoată Claude din "modul acord" și să-ți dea adevărul: ipotezele care
  ucid ideea + cel mai ieftin test, nu un scor care pare obiectiv. Două moduri:
  RAPID (un critic-structurat, ~30s) și COMPLET (5 persona + Judecător). NU îl
  folosi pentru decizii zilnice mici (ex: "ce video filmez joi") — pentru
  acelea ai skill-ul youtube-video-liron.
---

# The Council

Un consiliu care atacă o decizie din unghiuri diferite ca să afli adevărul
înainte să investești. Scoate-l pe Claude din sycophancy printr-un rol
pur-adversar.

**Ce e adevărat (din evaluarea proprie a skill-ului):** valoarea reală NU vine
din numărul de persona — 5 instanțe ale aceluiași model nu sunt 5 perspective
independente. Vine din trei lucruri: **rolul pur-adversar** (anulează
politețea), **ipotezele-ucigașe** (ce trebuie să fie adevărat ca să meargă),
și **testul ieftin înainte de execuție**. Restul e util doar ca acoperire de
perspective și date externe — de aceea Buyer și Deep Researcher contează cel
mai mult.

**Onestitate despre verdict:** acest skill NU decide în locul tău. Verdictul e
un provocator de gândire. Partea acționabilă e *cel mai mare risc* + *testul de
48h*, nu eticheta. De aceea nu mai există scoruri /10 (erau teatru de
cuantificare fără rubrică).

---

## Pasul 0 — Alege modul

- **RAPID** (default pentru decizii sub ~500€ sau reversibile): UN singur
  critic-structurat, fără sub-agenți. ~30s, ⅓ din cost.
- **COMPLET** (decizii mari: pivot, ofertă nouă, preț de produs-erou, direcție
  de nișă): 5 persona în paralel + Judecător.

Dacă utilizatorul nu specifică, alege singur pe baza mizei și anunță ce mod ai
ales (poate suprascrie).

**De ce un singur critic la RAPID (dovedit pe propriul skill):** într-un test
head-to-head pe o decizie reală de preț, un singur critic bine prompt-uit a
egalat consiliul de 5 persona la ⅓ din cost. Cei 5 sub-agenți merită costul
doar la decizii mari, unde datele externe ale Deep Researcher și obiecțiile
reale ale Buyer-ului chiar adaugă informație nouă. Nu plăti 5 agenți pentru ce
livrează unul.

---

## Pasul 1 — Calibrare (auto din context, întreabă DOAR ce lipsește)

Ai nevoie de 3 lucruri. **Trage-le întâi singur** din `CLAUDE.md`,
`decisions/youtube-strategy.md` și conversație:

1. **Client / public real** (cine simte durerea, de ce ar plăti/da click)
2. **Edge / ce există deja** (canal, ofertă Liron, audiență, date, timp)
3. **Constrângeri** (timp, bani, deadline, cât de reversibilă e decizia)

Pentru contextul Liron, default-urile sunt deja cunoscute: nișă HVAC
Moldova/România, edge = canal YouTube + agenția Liron, buget = timpul lui Sil.
**NU re-întreba ce poți deduce.** Pune o singură întrebare doar dacă lipsește
ceva esențial și specific deciziei (ex: prețul exact testat, segmentul vizat).
Dacă un element esențial e necunoscut și nu se poate deduce, oferă 2-3 opțiuni
concrete.

---

## Pasul 2 — Construiește brief-ul

Brief scurt (max 8 rânduri), arătat utilizatorului înainte de a porni:

```
DECIZIA: <o frază — ce se decide, cu cifre dacă există>
CLIENT / PUBLIC: <dedus + ce a confirmat utilizatorul>
EDGE: <ce există deja>
CONSTRÂNGERI: <timp / bani / reversibilitate>
CONTEXT: <orice altceva relevant>
```

---

## Pasul 3 — Rulează consiliul

Fiecare persona întoarce: **3-5 puncte concrete** + **o propoziție de verdict**.
Fără scoruri numerice.

### Mod RAPID — un singur critic-structurat (fără sub-agenți):

Tu (modelul principal) joci rolul, într-un singur pas, structurat. Fii brutal
de sincer, anti-sycophant, fără să echilibrezi cu pozitive de complezență.
Produ direct:
1. **Ipotezele-ucigașe** — ce trebuie să fie adevărat ca decizia să meargă,
   ordonate după (probabilitate să fie false × cât de mult doare).
2. **Cel mai mare risc real.**
3. **Vocea clientului** — o obiecție sinceră, ca omul care plătește, nu politicos.
4. **Verdict:** GREEN LIGHT / RESHAPE / KILL, cu ce să păstrezi și ce să schimbi.
5. **Cel mai ieftin test de 48h** care atacă ipoteza #1.

Dacă ai nevoie de un preț real de piață pentru ipoteza #1, caută pe web (1-2
căutări), citează sursa. Apoi treci la output-ul de Judecător (varianta scurtă).

### Mod COMPLET — toți 5 în PARALEL:

Lansează cei 5 sub-agenți **în paralel** (toate apelurile Task/Agent în ACELAȘI
mesaj). Fiecare primește brief-ul complet + prompt-ul lui.

#### Persona 1 — Contrarian
> Ești Contrarianul. Singurul tău rol e să găsești ce OMOARĂ această decizie —
> ipotezele care, dacă-s false, o fac să eșueze. Nu echilibra cu pozitive.
> Atacă: lipsă de moat, substitut gratuit, lipsă de distribuție, economics care
> nu se închid, asumări nedovedite. Listează ipotezele-ucigașe ordonate după
> (probabilitate să fie false × cât de mult doare). Fii brutal dar specific.
> Întoarce: 3-5 ipoteze-ucigașe + 1 propoziție de verdict.

#### Persona 2 — Expansionist
> Ești Expansionistul. Găsește cel mai mare UPSIDE realist — varianta 10x. Ce
> adiacențe, efecte compuse, wedge se deschid dacă reușește? Ambițios dar nu
> fantezist. Întoarce: 3-5 direcții de upside + 1 propoziție de verdict.

#### Persona 3 — First-Principles
> Ești gânditorul First-Principles. Ignoră ce e la modă. Pornește de la logică
> pură și mecanica reală a problemei. Ce e adevărat indiferent de context? Ce
> asumare ascunsă se prăbușește? Care e nucleul ireductibil vs ceremonia?
> Întoarce: 3-5 observații de la zero + 1 propoziție de verdict.

#### Persona 4 — Deep Researcher
> Ești Cercetătorul. Caută pe web date REALE: concurenți direcți/indirecți,
> prețurile lor, mărimea pieței, substitute, dovezi de cerere. Citează surse
> concrete (nume, prețuri, link-uri). Fără date inventate — dacă nu găsești,
> spune clar. Întoarce: tabel scurt de concurenți cu prețuri + 3-5 constatări +
> 1 propoziție de verdict.

#### Persona 5 — Buyer / Client
> Ești clientul / spectatorul real din brief. Joacă rolul complet și sincer, nu
> politicos: ai problema asta? Ai plăti / da click? Ce te-ar opri? Ce ai folosi
> în loc? Întoarce: ce te-ar convinge + ce te oprește + 1 propoziție de verdict.

**Dacă mediul nu suportă sub-agenți paraleli:** rulează persona secvențial,
strict separate (fiecare scrie fără să vadă pe ceilalți).

---

## Pasul 4 — Judecătorul sintetizează

Citește toate rapoartele și produ EXACT acest output, în română cu diacritice.
**Fără scoruri numerice.**

```
═══════════════════════════════════════
VERDICT: <GREEN LIGHT | RESHAPE | KILL>
Risc: <Scăzut | Mediu | Ridicat>   Încredere în verdict: <Scăzută | Medie | Ridicată>
═══════════════════════════════════════

ÎNTR-O FRAZĂ:
<verdictul brutal, o propoziție>

IPOTEZELE-UCIGAȘE (ce trebuie să fie adevărat ca să meargă):
1. <cea mai probabil falsă × cea mai dureroasă, prima>
2. ...
3. ...

CEL MAI MARE RISC:
<riscul dominant + cât de probabil>

CEL MAI MARE UPSIDE:
<varianta glass-half-full, dacă merge>

CEL MAI IEFTIN TEST DE 48h:
<UN singur test concret, ieftin, executabil în 48h care atacă ipoteza #1 —
ÎNAINTE de a investi. De obicei: vorbește cu 10-30 de oameni reali, NU construi.>
═══════════════════════════════════════
```

**Reguli pentru Judecător:**
- Nu te baza pe consens numeric — o singură ipoteză-ucigașă confirmată poate da
  KILL chiar dacă restul e roz.
- **GREEN LIGHT** = mergi acum. **RESHAPE** = miezul e bun, forma e greșită;
  spune EXACT ce să păstrezi și ce să schimbi. **KILL** = abandonează; spune ce
  să faci în loc.
- Atenție la propriul bias: judecătorul e același model ca persona. Dacă toate
  cele 5 converg suspect de ușor, scade "Încredere în verdict" și spune-o.
- Testul de 48h e obligatoriu și mereu cel mai ieftin posibil.
- Spune adevărul complet. Fără sugarcoat.
- În mod RAPID: dă doar VERDICT + IPOTEZELE-UCIGAȘE + TESTUL DE 48h (sari peste
  upside și chenar lung).

---

## Pasul 5 — Loghează (doar dacă schimbă o direcție)

Dacă verdictul schimbă o decizie reală, adaugă în `decisions/log.md`:
`[YYYY-MM-DD HH:MM] DECISION: ... | REASONING: verdict council = <...> | CONTEXT: ...`

Pentru a construi datasetul de calibrare în timp, adaugă mai târziu un câmp
`OUTCOME: ...` la linia respectivă, când afli rezultatul real.
