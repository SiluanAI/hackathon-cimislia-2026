# Liron — Producție YouTube (nișa HVAC)

Repo de lucru pentru canalul de YouTube al **Liron Agency**. Conține skill-urile,
strategia și pachetele complete de video — tot ce trebuie pentru a publica, în
afară de filmare.

**Echipă:** Sil (Siluan Lipădatu) + Vania (Ion Văleanu)
**Nișă:** patroni de firme HVAC din Moldova și România

---

## De unde începi

1. `decisions/youtube-strategy.md` — digest complet: nișă, reguli de algoritm,
   workflow thumbnail, ofertă Liron, plan de publicare, research piață.
2. `youtube/README.md` — index cu toate pachetele video și statusul lor.
3. `CLAUDE.md` — brain-ul asistentului (reguli de lucru și comunicare).

## Skill-uri

- `.claude/skills/youtube-video-liron/` — produce pachetul complet pentru un video
  (idee → scenariu → thumbnail → titlu → descriere → playlist → post de lansare).
- `.claude/skills/council/` — stress-testează o idee cu un consiliu adversarial
  (Contrarian, Expansionist, First-Principles, Deep Researcher, Buyer + Judecător)
  înainte de a investi timp în ea.

## Structură

```
.claude/skills/   skill-uri (producție video + council)
youtube/          pachete video + evoluția strategiei
decisions/        decision log + digest de strategie
```
