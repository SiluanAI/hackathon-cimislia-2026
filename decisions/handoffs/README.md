# Handoffs de sesiune

Predări de sesiune scrise de skill-ul `session-handoff` (anti context-rot).

## Convenție de denumire
```
YYYY-MM-DD-HHMM-<topic-slug>.md
```
Prefixul dată-oră sortează fișierele cronologic — cel mai recent e ultimul la listare.

## Cum reia o sesiune nouă
1. `git pull`
2. Listează acest folder.
3. Citește cel mai RECENT fișier cu `Status: ACTIV` și continuă din "REIA DE AICI".
4. Dacă sunt mai multe fire active sau ți s-a cerut un topic anume, citește fișierul
   cu acel topic în nume.

## Reguli
- Rulează handoff la **225.000 tokeni**; plafon dur **250.000** (niciodată depășit).
- Marchează un handoff `Status: ÎNCHIS` când firul e terminat.
- Handoff-ul salvează contextul, nu fișierele — persistența reală = commit + push.
