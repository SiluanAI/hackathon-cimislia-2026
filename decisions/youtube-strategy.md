# Strategia YouTube Liron Agency — digest pentru sesiuni viitoare

Acest fișier rezumă tot ce s-a decis și construit pentru canalul de YouTube al
Liron Agency, ca orice sesiune Claude Code viitoare să continue fără context pierdut.
Skill-ul complet: `.claude/skills/youtube-video-liron/`.

## Nișa (validată CGE Niche Validator)

**Niche Hypothesis Statement:** "Îi ajut pe patronii de firme HVAC din Moldova și
România să nu mai piardă clienți."

- Audiență: patron de firmă HVAC/instalații, 35-55 ani, bun la meserie/slab la digital.
- Piață: Moldova întâi, apoi România. Nișa e GOALĂ în RO/MD, DOVEDITĂ în EN.
- Sil apare pe cameră, vorbește română cu diacritice.
- Poziționare: **Expert-Enthusiast Hybrid** — "Cum am făcut eu X pentru un client HVAC",
  NU "Cel mai bun mod de a face meseria". Ton de coleg, nu guru.

## Principii de algoritm (regulile, nu opțiuni)

- CTR + Retenție decid totul. Thumbnail+titlu = ~50% din efort.
- **Trifecta (Shane Hummus):** titlu + thumbnail + intro trebuie congruente, aceeași
  direcție. Incongruența ucide retenția.
- Hook în primele 15s, fără intro.
- Un video = o singură durere. Bucle deschise la 30-60s.
- Metrica de succes = LEAD-ul, nu vederile (B2B mic).
- Format canonic: **EXPLAINER** (~80%), nu Listicle — vinde high-ticket/B2B.
- King of the puddle: îngustează tare pe HVAC, lărgești după ce câștigi.
- Consistență 1 video/săptămână.

## Workflow thumbnail

- Tool: **ChatGPT** (Thumbmagic replicat în conversație). Sil pune scriptul → ChatGPT
  face thumbnail-ul. Instrucțiunea de brand e în `references/thumbnail-template.md`.
- **Regula de aur: text minim** — max 3-4 cuvinte overlay. Fără liste de etichete.
- Constante de brand: identitatea lui Sil, lumină violet pe o parte, fundal grid întunecat.

## Format descriere (reguli)

- Link ca `liron.md` (fără https — nu se face clickabil oricum).
- Capitole FĂRĂ timecode — doar repere ca etichete simple.
- Structură: hook 2 rânduri → ce e în video → "Sunt Siluan..." → CTA liron.md +
  contact +373 78 996 237 → CAPITOLE (repere) → hashtags.

## Oferta Liron (ancoră pentru CTA — date reale)

- Site Prezentare 500€ · **Site cu Programare 800€ (produs-erou HVAC)** · E-commerce 1400€
- Chatbot Basic 300€ · Chatbot AI Smart 800€ · AI Agent 1500€
- Strategy Session 350€ · AI Audit 1200€ · Enterprise 2500€+
- Client HVAC de referință: Ecoconfortsistem (Hîncești). Date: 4-10 apeluri/zi,
  lucrare medie 8.000 lei, program 8:00-20:00, pierde clienți din apeluri ratate.
  Site construit în 3 zile, și-a scos investiția în 3 luni.

## Plan de publicare

**Programate (filmate):**
- #1 — Câți clienți pierde o firmă fără sistem (calcul live)
- #15 (25 iun) — Cum primește clientul programare automat (whiteboard)
- #21 (26 iun) — Site Ecoconfortsistem construit în 3 zile
- #11 (28 iun) — Ce e un chatbot și cum prinde clienții noaptea
- #4 (30 iun) — "Nu am nevoie de site" — calcul live (~1.000.000 lei/an)

**De filmat (pachete scrise, gata):**
- #18 (reframe) — "Clienții mei nu vor folosi online" — răspuns la 3 frici
- Video A (#6) — De ce un instalator mai slab apare înaintea ta pe Google
- Video B (#47) — Sezonul de AC: cine se pregătește acum câștigă vara
- Video C (recenzii) — Zeci de recenzii Google fără să ceri manual (sistem SMS automat)

**Amânat:** #31 (agenție AI la 18 ani — personal brand) după 8-10 videouri HVAC.
**Anulat:** #8.

## Research piață (dovezi)

Nișa e dovedită în EN, goală în RO/MD. Teme validate prin videouri concurente:
- GMB/Google local HVAC: masiv dovedit (ServiceTitan + zeci de creatori).
- Recenzii Google HVAC: videouri constante 2018→2026.
- Sezon AC: vara = până la 50% din vânzări anuale.
- Diferențiatorul Liron vs. modelele EN: ele sunt DIY-tutorial; noi vindem
  done-for-you + automatizare AI. Plus suntem primii în română.
- Mystery-shopper ("am sunat 5 firme") = unghi SLAB pentru business (doar scam-exposé
  în EN). Evitat.

## Note operaționale

- Push git eșuează cu 403 (sesiune web fără permisiune write / politică egress).
  Munca e comisă local pe `claude/practical-heisenberg-isoprv`. Pentru persistență:
  acordă write integrării GitHub sau rulează o sesiune locală.
- Commituri: author/committer = noreply@anthropic.com (corect). Lipsește doar
  semnătura GPG — limitare de mediu, nu se poate adăuga fără cheie.
