═══════════════ SESSION HANDOFF ═══════════════
Data: 2026-06-29 05:30  ·  Topic: Plan master + motorul build→demo
Branch: claude/practical-heisenberg-isoprv  ·  Repo: Liron YouTube  ·  Status: ÎNCHIS (continuat în handoff-ul 2026-06-29-2000)

DE UNDE AM PORNIT (obiectivul sesiunii):
Continuarea strategiei YouTube HVAC: producerea pachetelor de video pentru luna,
rafinarea skill-ului, și definirea unui plan structurat pentru un nou motor de conținut
"build→demo" (construim unelte reale, le demonstrăm pe cameră).

CE S-A LIVRAT:
- Integrat în skill: Niche Hypothesis Statement, Expert-Enthusiast, format Explainer,
  king of the puddle, Trifecta (titlu+thumbnail+intro congruente).
- Thumbnail workflow schimbat definitiv: ChatGPT din script, max 3-4 cuvinte text
  (promptul de imagine din skill ELIMINAT, înlocuit cu instrucțiune reutilizabilă).
- Descriere: link `liron.md` fără https, capitole ca repere fără timecode.
- 9 videouri filmate și PROGRAMATE (25 iun → 10 iul). Pachete în `youtube/pachete/`.
- Research cu proof (Google Maps, recenzii, sezon AC dovedite în EN; mystery-shopper
  abandonat ca slab).
- `youtube/build-demo-backlog.md` — 7 unelte construibile (B1-B7) cu proof.
- `youtube/plan-master.md` — planul unic în 3 faze.
- Git push DEBLOCAT: Sil a instalat GitHub App "Claude" cu write pe repo.

DECIZII BLOCATE (nu le redeschide fără motiv):
- Build: Sil construiește uneltele ÎMPREUNĂ cu Claude, aici, înainte de filmare.
- Ritm build→demo: 1 unealtă + 1 demo/săptămână, ÎNCEPÂND după 10 iul.
- Caz de test: ecoconfortsistem (client HVAC real).
- Stack: ales de Claude, pragmatic per unealtă.
- Ordinea uneltelor: B1 Estimator AI preț → B2 Chatbot → B5 Recenzii → B3 Apel ratat...
- #8 anulat, #31 amânat după 8-10 videouri HVAC, #18 reframuit (obiecții programare).

FIȘIERE CHEIE (unde să te uiți):
- `youtube/plan-master.md` — firul director, cele 3 faze.
- `youtube/build-demo-backlog.md` — uneltele B1-B7 + ordine + proof.
- `youtube/pachete/` (9 fișiere) + `youtube/README.md` — pachetele video + index.
- `youtube/evolutie.md` — cum a evoluat strategia.
- `.claude/skills/youtube-video-liron/` — skill-ul de producție (SKILL.md + references/).
- `decisions/youtube-strategy.md` — digest strategie.

STARE GIT:
- Branch: claude/practical-heisenberg-isoprv · Ultim commit: 9a3e4d8 "docs: add master plan..."
- Necomis: nu · Push-uit: da (totul e pe GitHub).

VERIFICAT (confirmat vs neconfirmat):
- Push funcționează (confirmat după instalarea GitHub App). / Thumbnail-urile generate
  de ChatGPT arată bine (confirmat din screenshots Sil).
- NEVERIFICAT: nicio unealtă build→demo nu e încă construită; CTR/retenția videourilor
  (toate Scheduled, 0 vederi).

AMÂNAT / ÎNTREBĂRI DESCHISE:
- Scenariile complete pentru #1 și #11 nu sunt reconstituite în `pachete/` (doar repere) —
  Sil poate cere reconstrucția dacă vrea.

REIA DE AICI (primul pas concret în sesiunea nouă):
1. Pornește Faza B: B1 — Estimator AI de preț pentru HVAC.
2. Claude propune spec scurt + alege stack, apoi construiește ÎMPREUNĂ cu Sil aici,
   testat pe ecoconfortsistem. Apoi Sil filmează demo-ul → skill youtube-video-liron.
═══════════════════════════════════════════════
