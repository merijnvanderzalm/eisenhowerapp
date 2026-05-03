# eisenhowerapp

# Eisenhower Matrix PWA

Een iPhone-klare Progressive Web App voor de Eisenhower Matrix, aangestuurd door Claude AI.

## Bestanden

```
eisenhower-pwa/
├── index.html      ← de volledige app
├── manifest.json   ← PWA-configuratie
├── sw.js           ← service worker (offline)
└── README.md
```

> **Optioneel:** Voeg `icon-192.png` en `icon-512.png` toe (jouw logo) voor een mooi icoontje op het thuisscherm.

---

## Stap 1 — Zet op GitHub Pages

1. Maak een nieuw repository aan op github.com (bijv. `eisenhower-matrix`)
2. Upload de drie bestanden (`index.html`, `manifest.json`, `sw.js`)
3. Ga naar **Settings → Pages → Source: main branch / root**
4. Jouw app staat op: `https://jouwgebruikersnaam.github.io/eisenhower-matrix/`

---

## Stap 2 — API key instellen

Open `index.html` en zoek naar:

```
headers: { 'Content-Type': 'application/json' },
```

Voeg daar **direct onder** je Anthropic API key toe:

```javascript
headers: {
  'Content-Type': 'application/json',
  'x-api-key': 'sk-ant-api03-JOUW-KEY-HIER',
  'anthropic-version': '2023-06-01',
  'anthropic-dangerous-direct-browser-calls': 'true'
},
```

Je key vind je op: https://console.anthropic.com/

---

## Stap 3 — Toevoegen aan iPhone thuisscherm

1. Open Safari op je iPhone
2. Ga naar jouw GitHub Pages URL
3. Tik op het **Deel-icoon** (vierkantje met pijl omhoog)
4. Kies **"Voeg toe aan thuisscherm"**
5. Tik **Voeg toe** — klaar!

De app opent nu als een volledige app zonder adresbalk, werkt offline, en sla alle taken op in je iPhone.

---

## Gebruik

- **Taak toevoegen:** Typ een beschrijving (vertel ook of het urgent/belangrijk is) → tik **+**
- **Verplaatsen:** Houd een taak ingedrukt (0.4s) → sleep naar een ander kwadrant
- **Afvinken:** Tik op het vakje links van een taak
- **Archiveren:** Tik op **×** naast een taak
- **Archief bekijken:** Tik op **📦 Archief** rechtsboven
- **Verwijderen:** Open archief → tik **✕** naast een taak
