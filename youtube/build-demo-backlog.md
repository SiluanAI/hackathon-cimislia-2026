# Backlog "Build → Demo" — unelte HVAC pe care le construim și le filmăm

Motorul de conținut nou: NU vorbim despre concepte, CONSTRUIM o unealtă reală (eu + Sil
în Claude Code) și o demonstrăm pe cameră. Demo cu ceva care merge = dovadă, nu promisiune.
Poziționare Expert-Enthusiast: "Uite ce am construit pentru o firmă HVAC."

## Durerile validate (din research, cu proof)
- Firmele HVAC ratează ~30% din apeluri — ocupate fix când sună clienții.
- Fiecare minut fără răspuns = client pierdut la concurent. Nevoie: răspuns în 60s.
- Follow-up inconsecvent (apeluri ratate, oferte fără răspuns, cereri de recenzie).
- Recenziile = factorul #1 în alegerea unei firme locale.
- Estimări instant = rată de câștig mai mare.

Surse:
- https://www.achrnews.com/articles/166287-missed-calls-lost-jobs-why-hvac-companies-are-adopting-voice-ai-agents
- https://aiemployees.us/blog/hvac-missed-call-ai-workflow
- https://www.servicetitan.com/industries/hvac-software

## Unelte construibile (fiecare = un video demo)

| # | Unealtă | Ce construim | Demo video | Proof | Efort |
|---|---------|--------------|------------|-------|-------|
| B1 | Estimator AI de preț | Pagină web: clientul alege tip lucrare + BTU/detalii → preț orientativ instant + buton programare | "Am construit un calculator care dă clientului prețul în 10 secunde" | quote-gen AI validat (ServiceTitan) | Mic |
| B2 | Chatbot HVAC pe site | Widget chat: răspunde FAQ, calculează, capturează lead, propune programare | "Am pus un angajat virtual pe site-ul unei firme HVAC" | AI receptionist validat masiv | Mic-mediu |
| B3 | Răspuns automat la apel ratat | Apel ratat → SMS automat în 60s ("ne pare rău, programați aici") | "Sistemul care prinde clientul în 60s după un apel ratat" | missed-call textback validat | Mediu (necesită Twilio/SMS) |
| B4 | Sistem de programare | Calendar + sloturi + confirmare email/SMS + notificare patron | "Cum arată un sistem de programare pentru HVAC (live)" | product-hero Liron 800€ | Mediu |
| B5 | Cerere recenzie automată | După lucrare → SMS cu link direct de recenzie | "Sistemul care cere recenzii singur după fiecare lucrare" | review automation validat | Mic-mediu |
| B6 | Mini-dashboard lead-uri | Panou simplu: lead-uri din site/chat, status, urmărire | "Mi-am făcut un mini-CRM pentru lead-uri HVAC" | lead tracking validat | Mediu |
| B7 | Reminder de mentenanță sezonier | Automatizare: mesaj clienților vechi înainte de sezon ("verificare AC?") | "Cum scoți bani din clienții vechi automat, înainte de vară" | seasonal re-engagement validat | Mic |

## Recomandare de ordine
1. **B1 Estimator AI de preț** — primul. Pur web, îl construim repede, demo spectaculos
   (cifra apare instant pe ecran), zero dependențe externe.
2. **B2 Chatbot HVAC** — al doilea, se leagă natural de B1.
3. **B5 Recenzii** / **B3 Apel ratat** — după, când adăugăm SMS (Twilio).

## Cum lucrăm
- Eu propun unealta + spec, o construim împreună în Claude Code (Vania poate prelua codul).
- O testăm pe un caz HVAC (ecoconfortsistem sau demo).
- Filmezi demo-ul → pachet complet de video (skill youtube-video-liron).
- Fiecare unealtă demonstrată e și un produs vandabil = lead direct.
