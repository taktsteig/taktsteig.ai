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
