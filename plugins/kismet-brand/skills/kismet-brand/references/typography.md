# Kismet — Tipografía

## Fuentes disponibles

**Cómo cargarlas:** Lee el archivo `assets/fonts.css` e inyéctalo dentro de `<style>` en cualquier HTML/SVG, o como `<style>{fontCss}</style>` en React.

```js
// Ejemplo en React
import { useEffect, useState } from 'react';

function KismetApp() {
  const [fontCss, setFontCss] = useState('');
  // El contenido de assets/fonts.css se inyecta aquí
  return (
    <>
      <style>{fontCss}</style>
      {/* tu componente */}
    </>
  );
}
```

---

## Chillax — Tipografía Principal

| Weight name | font-weight | Uso |
|---|---|---|
| Extralight | 200 | Decorativo, quotes grandes |
| Light | 300 | Subtítulos secundarios |
| Regular | 400 | H2, subtítulos |
| Medium | 500 | H3, títulos de cards |
| Semibold | 600 | CTA buttons, etiquetas importantes |
| Bold | 700 | Display, H1, headlines principales |

**Aplica en:** logotipo, branding, títulos, subtítulos, CTA buttons, frases destacadas, posts de RRSS.

---

## Synonym — Tipografía Secundaria

| Weight name | font-weight | Uso |
|---|---|---|
| Extralight | 200 | Raro, solo decorativo |
| Light | 300 | Texto largo, captions |
| Regular | 400 | Párrafos, cuerpo de texto |
| Medium | 500 | UI labels, énfasis suave |
| Semibold | 600 | Énfasis en cuerpo, destacados |
| Bold | 700 | Énfasis fuerte en texto corrido |

**Aplica en:** párrafos, descripciones, metadata, UI labels, captions, texto de formularios.

---

## Jerarquía completa

```css
/* ── Títulos (siempre Chillax) ── */
.kismet-display {
  font-family: 'Chillax', sans-serif;
  font-weight: 700;
  font-size: clamp(3rem, 6vw, 5rem);
  line-height: 1.05;
  letter-spacing: -0.01em;
}
.kismet-h1 {
  font-family: 'Chillax', sans-serif;
  font-weight: 700;
  font-size: clamp(2rem, 4vw, 3rem);
  line-height: 1.15;
}
.kismet-h2 {
  font-family: 'Chillax', sans-serif;
  font-weight: 400;
  font-size: clamp(1.5rem, 3vw, 2.25rem);
  line-height: 1.2;
}
.kismet-h3 {
  font-family: 'Chillax', sans-serif;
  font-weight: 500;
  font-size: 1.5rem;
  line-height: 1.3;
}
.kismet-cta {
  font-family: 'Chillax', sans-serif;
  font-weight: 600;
  font-size: 1rem;
  letter-spacing: 0.02em;
}

/* ── Cuerpo (siempre Synonym) ── */
.kismet-body-lg {
  font-family: 'Synonym', sans-serif;
  font-weight: 400;
  font-size: 1.25rem;
  line-height: 1.65;
}
.kismet-body {
  font-family: 'Synonym', sans-serif;
  font-weight: 400;
  font-size: 1rem;
  line-height: 1.65;
}
.kismet-body-sm {
  font-family: 'Synonym', sans-serif;
  font-weight: 300;
  font-size: 0.875rem;
  line-height: 1.6;
}
.kismet-label {
  font-family: 'Synonym', sans-serif;
  font-weight: 500;
  font-size: 0.75rem;
  letter-spacing: 0.03em;
  text-transform: uppercase;
}
```

## Reglas tipográficas

- Nunca mezclar Chillax y Synonym en la misma línea
- Chillax para títulos/CTAs — Synonym para todo texto de lectura
- Interlineado títulos: 1.1–1.3 | cuerpo: 1.6–1.7
- Tracking en displays grandes: `-0.01em` a `0em`
- Color texto principal: `#141414` sobre fondos claros
- Color texto sobre oscuro: `#e5e5e5`
- Color texto secundario: `#959684` (olive-500)
- Color texto muted: `#b0b0a3` (olive-300)
