# Kismet — Colorimetría y Sistema UI

---

## PALETA OFICIAL COMPLETA (16 tonos)

```css
:root {
  /* ── Familia Olive (estructural, contraste fuerte) ── */
  --olive-900: #626148;   /* rgb(98,97,72)    hsl(59,15%,33%)  — fondo oscuro, botones CTA, publicidad */
  --olive-700: #7c7b67;   /* rgb(124,123,103) hsl(61,9%,45%)   — footer, secciones medias */
  --olive-500: #959684;   /* rgb(149,150,132) hsl(65,8%,55%)   — iconos, elementos secundarios */
  --olive-300: #b0b0a3;   /* rgb(176,176,163) hsl(65,7%,66%)   — texto muted, placeholders */

  /* ── Familia Earth (calidez, cercanía) ── */
  --earth-900: #ada796;   /* rgb(173,167,150) hsl(41,13%,63%)  — fondos cálidos oscuros */
  --earth-700: #d0c8b4;   /* rgb(208,200,180) hsl(42,22%,76%)  — cards, superficies */
  --earth-500: #d8d2bf;   /* rgb(216,210,191) hsl(43,21%,80%)  — fondos de sección */
  --earth-300: #e1dacd;   /* rgb(225,218,205) hsl(40,22%,84%)  — fondo principal de página */

  /* ── Familia Sage (verde-gris natural, frescura) ── */
  --sage-900:  #a4aba0;   /* rgb(164,171,160) hsl(108,5%,65%)  — acento verde, Kisma body */
  --sage-700:  #b4bab1;   /* rgb(180,186,177) hsl(108,5%,71%)  — superficies con toque verde */
  --sage-500:  #c2c7c1;   /* rgb(194,199,193) hsl(114,5%,77%)  — fondos suaves */
  --sage-300:  #d1d4cf;   /* rgb(209,212,207) hsl(108,4%,82%)  — casi neutro con verde */

  /* ── Familia Neutral (base, legibilidad) ── */
  --neutral-900: #cbcbcb; /* rgb(203,203,203) hsl(0,0%,80%)    — texto secundario sobre claro */
  --neutral-700: #d4d4d4; /* rgb(212,212,212) hsl(0,0%,83%)    — bordes, líneas divisorias */
  --neutral-500: #dcdcdc; /* rgb(220,220,220) hsl(0,0%,86%)    — fondos neutros */
  --neutral-300: #e5e5e5; /* rgb(229,229,229) hsl(0,0%,90%)    — fondo claro principal */

  /* ── Monocromático (exclusivo para logotipo y texto) ── */
  --brand-black: #141414; /* rgb(20,20,20)    — logo positivo, texto principal */
  --brand-white: #e5e5e5; /* rgb(229,229,229) — logo negativo, texto sobre fondos oscuros */

  /* ── Alias semánticos UI ── */
  --bg-page:     var(--earth-300);
  --bg-section:  var(--neutral-300);
  --bg-card:     var(--earth-700);
  --bg-dark:     var(--olive-900);
  --bg-mid:      var(--sage-500);
  --text-main:   var(--brand-black);
  --text-sub:    var(--olive-500);
  --text-muted:  var(--olive-300);
  --text-ondark: var(--brand-white);
  --border:      var(--neutral-700);
  --border-soft: var(--neutral-500);
  --accent:      var(--olive-900);
  --accent-alt:  var(--sage-900);
}
```

## COMBOS PRE-APROBADOS

| Nombre | Fondo | Texto | Acento | Uso |
|---|---|---|---|---|
| **Campo** | `#e1dacd` | `#141414` | `#626148` | Web principal, landing pages |
| **Bosque** | `#626148` | `#e5e5e5` | `#b4bab1` | Hero sections, publicidad |
| **Niebla** | `#e5e5e5` | `#141414` | `#7c7b67` | App UI, interfaces limpias |
| **Tierra** | `#ada796` | `#e5e5e5` | `#e1dacd` | Posts RRSS, materiales cálidos |
| **Salvia** | `#a4aba0` | `#141414` | `#626148` | Cards de servicios |

## REGLAS CROMÁTICAS

✅ Siempre mezclar mínimo 2 familias de color  
✅ Logo blanco (`#e5e5e5`) sobre fondos oscuros de la paleta  
✅ Logo negro (`#141414`) sobre fondos claros de la paleta  
❌ NUNCA negro puro `#000000` ni blanco puro `#ffffff`  
❌ NUNCA colores saturados ni fuera de la paleta  
❌ NUNCA esquema monocromático en piezas  
❌ NUNCA azules, rojos, amarillos u otros colores no aprobados  

---

## SISTEMA DE SECCIONES WEB

| Sección | Background | Texto | Notas |
|---|---|---|---|
| Navbar | `olive-900` | `brand-white` | Synonym Regular |
| Hero | `olive-900` + foto overlay 40% | `brand-white` | Chillax Bold, CTA pill |
| Sección principal | `earth-300` | `brand-black` | |
| Sección alterna | `neutral-300` | `brand-black` | |
| Cards / Features | `earth-700` | `brand-black` | border-radius 16px |
| CTA Strip | `sage-900` | `brand-black` | |
| Footer | `olive-700` | `brand-white` | |

---

## COMPONENTES UI BASE

```css
/* ─── Botón Principal ─── */
.btn-primary {
  display: inline-flex; align-items: center; justify-content: center;
  background-color: var(--olive-900);
  color: var(--brand-white);
  font-family: 'Chillax', sans-serif;
  font-weight: 600; font-size: 1rem;
  padding: 14px 32px;
  border-radius: 999px; border: none; cursor: pointer;
  letter-spacing: 0.02em;
  transition: background 0.2s ease, transform 0.15s ease;
}
.btn-primary:hover { background-color: var(--olive-700); transform: translateY(-1px); }

/* ─── Botón Secundario (outline) ─── */
.btn-secondary {
  display: inline-flex; align-items: center; justify-content: center;
  background-color: transparent; color: var(--olive-900);
  font-family: 'Chillax', sans-serif;
  font-weight: 500; font-size: 1rem;
  padding: 13px 30px;
  border-radius: 999px; border: 1.5px solid var(--olive-900); cursor: pointer;
  transition: background 0.2s ease, color 0.2s ease;
}
.btn-secondary:hover { background-color: var(--olive-900); color: var(--brand-white); }

/* ─── Card ─── */
.card {
  background-color: var(--bg-card);
  border-radius: 16px; padding: 28px 24px;
  border: 1px solid var(--border-soft);
  box-shadow: 0 2px 16px rgba(98,97,72,0.08);
}

/* ─── Input ─── */
.input {
  font-family: 'Synonym', sans-serif; font-weight: 400; font-size: 1rem;
  color: var(--text-main); background-color: var(--neutral-300);
  border: 1.5px solid var(--border); border-radius: 12px;
  padding: 12px 16px; width: 100%; outline: none;
  transition: border-color 0.2s;
}
.input:focus { border-color: var(--olive-700); }

/* ─── Sombras ─── */
.shadow-sm { box-shadow: 0 1px 8px rgba(98,97,72,0.06); }
.shadow-md { box-shadow: 0 4px 24px rgba(98,97,72,0.10); }
.shadow-lg { box-shadow: 0 8px 40px rgba(98,97,72,0.14); }

/* ─── Secciones por color ─── */
.section-light   { background-color: var(--earth-300); }
.section-neutral { background-color: var(--neutral-300); }
.section-dark    { background-color: var(--olive-900); color: var(--brand-white); }
.section-sage    { background-color: var(--sage-500); }
.section-earth   { background-color: var(--earth-700); }
```

---

## TAMAÑOS MÍNIMOS DE LOGO

| Variante | Digital min. | Impreso min. |
|---|---|---|
| Logotipo completo | 135 × 73 px | 47 × 25 mm |
| Isotipo síntesis | 81 × 62 px | 28 × 21 mm |
| Kisma (mascota) | 74 × 81 px | 26 × 28 mm |

**Margen de seguridad:** zona libre en todos los lados = ~50% del alto total del logo.
