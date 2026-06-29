# Plan master — Liron Agency YouTube (nișa HVAC)

Planul unic care leagă TOT ce am construit. Nimic nu se aruncă: skill-ul, metoda de
package, cele 9 videouri programate, research-ul, backlog-ul build→demo. Acesta e firul
director peste toate.

## Decizii fixate (interviu Sil)
- **Build**: Sil construiește uneltele ÎMPREUNĂ cu Claude, aici, înainte de a filma.
- **Ritm build→demo**: 1 unealtă + 1 demo pe săptămână, ÎNCEPÂND după 10 iul 2026
  (după ce se epuizează cele 9 videouri deja programate).
- **Caz de test**: ecoconfortsistem (client HVAC real) — demo credibil cu date reale.
- **Stack**: ales de Claude, pragmatic per unealtă (rapid de construit + ușor de demonstrat).

## Cele 3 faze (NU se suprapun haotic — se înlănțuie)

### Faza A — în derulare (până 10 iul): videouri educative/durere
Cele 9 pachete deja filmate și programate (vezi `pachete/` + `README.md`).
25 iun → 10 iul. Acestea stabilesc nișa și durerea. NU le atingem.

### Faza B — de la 10 iul: motorul build→demo (1/săptămână)
Ordinea din `build-demo-backlog.md`, ancorată pe ecoconfortsistem:
1. **B1 Estimator AI de preț** (prima — pur web, demo spectaculos)
2. **B2 Chatbot HVAC** (se leagă de B1)
3. **B5 Cerere recenzie automată**
4. **B3 Răspuns automat la apel ratat** (când adăugăm SMS/Twilio)
5. **B4 Sistem de programare** (product-hero, demo live)
6. **B6 Mini-dashboard lead-uri**
7. **B7 Reminder mentenanță sezonier**

Ciclul săptămânal pentru fiecare unealtă:
1. Claude propune spec scurt + alege stack.
2. Sil + Claude construiesc unealta aici, în Claude Code.
3. Testăm pe ecoconfortsistem (date reale).
4. Sil filmează demo-ul.
5. Claude rulează skill-ul `youtube-video-liron` → pachet complet (același flux ca până acum).
6. Publicăm + logăm în `decisions/log.md`.

### Faza C — continuă: măsurare și iterație
După ce strâng vederi: ne uităm la CTR + retenție per video, vedem ce unghi prinde la
patronii HVAC, dublăm pe ce funcționează. Al doilea val din cele 100 idei + unelte noi.

## Reguli care rămân valabile peste tot (din skill)
- Metrica = LEAD, nu vederi. Format Explainer. Nișă strâns HVAC (king of the puddle).
- Trifecta: titlu + thumbnail + intro congruente.
- Thumbnail: ChatGPT din script, max 3-4 cuvinte text.
- Descriere: link `liron.md`, capitole ca repere fără timecode.
- Poziționare Expert-Enthusiast: "uite ce am construit eu pentru o firmă HVAC".
- Doar dovezi reale, fără cifre inventate.

## Avantajul modelului build→demo
Fiecare unealtă e simultan: (1) conținut demo cu dovadă vie, (2) produs vandabil, (3)
exercițiu real care îi crește lui Sil expertiza pe cameră. Demand-first rămâne: construim
doar unelte cu durere dovedită (toate B1-B7 au proof în backlog).

## Fișiere-cheie
- Skill producție: `.claude/skills/youtube-video-liron/`
- Pachete video: `youtube/pachete/` + `youtube/README.md`
- Backlog unelte: `youtube/build-demo-backlog.md`
- Evoluția strategiei: `youtube/evolutie.md`
- Digest pentru sesiuni noi: `decisions/youtube-strategy.md`
