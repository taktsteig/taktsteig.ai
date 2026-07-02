# Logo & Identity — taktsteig

## Prinzip

Das Logo von `taktsteig` ist:
- rein textbasiert
- ohne Icon
- ohne Farbflächen
- aber mit **einem einzigen Moment des Steigs**

Es zeigt:  
> **Minimalität mit Wirkung.**

---

## Darstellung

### Hauptform
taktsteig

Mit phonetischer Aussprache: `/ˈtaktʃˌʃtaɪ̯k/`

Das visuelle Merkmal:  
→ Ein **dünnner, roter Strich** am Ende des `g`,  
→ der sich in einem Winkel von **22° nach oben rechts** bewegt.

### Farben
- Text: `#0F1B2D` (Dark Blue) oder `#E0E0E0` (bei Dark Mode)
- Steig: `#E91E63` („Rising Red“)
- Phonetic: `#888`

### Schrift
- `Inter Medium`, fallback: `'Helvetica Neue', Arial, sans-serif`

---

## Technische Umsetzung

### CSS (für Web)
Der Aufstieg wird über `::after` realisiert:

```css
.rising-g::after {
  content: '';
  position: absolute;
  width: 7px;
  height: 1.8px;
  background: #E91E63;
  top: 53%;
  left: 100%;
  transform: translateY(-50%) rotate(22deg);
  transform-origin: left;
}

SVG
Siehe: assets/logo.svg

Warum kein Pfeil?
Der Aufstieg ist kein Symbol.
Er ist ein Moment im Verlauf.

Er soll nicht auffallen,
aber bleiben –
wie ein Takt, der sich hebt.

Verwendung
Auf Webseiten: als index.html mit integrierter Darstellung
In Terminal: taktsteig (Text nur), mit Erklärung im Kontext
In Dokumenten: mit logo.svg
Keine Logovariante ohne den Steig.
Denn: ohne Steig — kein taktsteig.



---

### ✅ 3. `assets/logo.svg`

> Skalierbares Vektor-Logo – für Docs, Social, Sharing

```xml
<svg width="400" height="100" viewBox="0 0 400 100" xmlns="http://www.w3.org/2000/svg">
  <!-- Styles -->
  <style>
    .text {
      font-family: 'Inter', 'Helvetica Neue', Arial, sans-serif;
      font-size: 64px;
      font-weight: 500;
      fill: #0F1B2D;
    }
    .phonetic {
      font-family: 'Inter', sans-serif;
      font-size: 20px;
      font-style: italic;
      fill: #888;
    }
    .rising-line {
      stroke: #E91E63;
      stroke-width: 2.4;
      stroke-linecap: round;
      fill: none;
    }
    @media (prefers-color-scheme: dark) {
      .text { fill: #E0E0E0; }
      .phonetic { fill: #AAA; }
    }
  </style>

  <!-- Haupttext: taktstei -->
  <text x="0" y="72" class="text">taktstei</text>

  <!-- Aufstieg am Ende des g -->
  <!-- Simuliert den Schwanz des g, der leicht nach oben geht -->
  <line x1="310" y1="68" x2="322" y2="62" class="rising-line" />

  <!-- Phonetics -->
  <text x="200" y="94" class="phonetic" text-anchor="middle">/ˈtaktʃˌʃtaɪ̯k/</text>
</svg>
```
