# Șablon prompt thumbnail (AI generează TOT, inclusiv textul)

Folosește poza de referință a lui Sil pentru identitate. Cere 1280x720, 16:9.
Cele 3 constante de brand (păstrează-le mereu): identitatea lui Sil, lumină
violet pe o parte, fundal grid întunecat + spațiu pentru text.

**Workflow confirmat:** Thumbmagic (generare) → ChatGPT (scoatere watermark).
Evită DALL-E pentru text — randează prost diacriticele.

Schimbă pentru fiecare video doar: POSE/expresia și TEXTUL.

```
A finished YouTube thumbnail, 1280x720px, 16:9 aspect ratio. Ready to publish.

SUBJECT: The exact same young man from the reference photo — same face, same
short reddish-brown hair, same sharp clean features. Replicate identity precisely.

POSE: [chest-up, body angled, hand gesture, expression matching the video emotion —
e.g. shocked/revealing, confident/explaining]. Direct eye contact with camera.

WARDROBE: fitted dark charcoal sweater, clean and modern.

LIGHTING: dramatic studio lighting. Strong white key light on one side of the face,
deep violet/purple rim light on the other. High contrast, hyper-realistic face.

BACKGROUND: deep dark navy-to-black gradient with faint glowing dark-purple geometric
grid lines, subtle violet glow in a corner. Subject clearly separated from background.

COMPOSITION: subject on the RIGHT half, LEFT half clear dark space for text.

TEXT ON IMAGE (render clearly and correctly, Romanian with diacritics):
- Top left, large bold white, tilted -2deg: "[NUMĂR/CUVÂNT ȘOC]"
- Below, slightly smaller, bright violet (#7C3AED): "[completarea]"
- Bottom left, small low-opacity white: "[cârlig curiozitate]"

TEXT STYLE: ultra-bold sans-serif (Anton/Bebas Neue), white with thin 2px black
outline. No other text on the image.

OVERALL: hyper-realistic photography, professional, vibrant, high contrast.
```
