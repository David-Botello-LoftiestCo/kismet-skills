---
name: kismet-brand
description: "Sistema completo de identidad de marca Kismet para generacion de piezas graficas, UI, web, redes sociales y comunicacion visual. Usa esta skill siempre que necesites crear cualquier pieza visual o de comunicacion para la marca Kismet — posts de Instagram, landing pages, componentes de app, publicidad, emails, presentaciones, o cualquier material que use el logotipo, colores, tipografias o personaje Kisma. Incluye SVG embebidos del logotipo y personaje Kisma, fuentes Chillax y Synonym en base64, paleta completa con valores HEX/RGB/HSL/CMYK, sistema de componentes UI, y guia de voz y tono. Tambien usala cuando el usuario pregunte sobre colores, tipografias, uso del logo, como usar a Kisma, o cualquier duda sobre las reglas de la marca."
---

# Kismet Brand Skill

Sistema completo de identidad visual de Kismet — clínica/plataforma de salud mental.

**Eslogan:** *sync your mind*  
**Posicionamiento:** Refugio digital de bienestar emocional. Empático, profesional, accesible.  
**Audiencia:** Adultos 22–45 años, digital-first, hispanohablante.

---

## Cómo usar esta skill

Para cualquier pieza de Kismet, sigue este orden:

1. **Fuentes** → Lee `assets/fonts.css` e inyéctalo en el `<style>` de la pieza
2. **Imágenes del logo o Kisma** → Utiliza los archivos ubicados en la carpeta `assets/logos/` (disponibles en PNG, JPG y SVG).
3. **Colores** → Usa las variables CSS de `references/colors-and-ui.md`
4. **Tipografía** → Consulta jerarquías en `references/typography.md`
5. **Tono y aplicaciones** → Consulta `references/voice-and-applications.md`

---

## Elementos de marca — resumen rápido

### Logotipo
- **viewBox:** `0 0 1000 554.49` (horizontal ~1.8:1)
- **Variantes de color:** negro `#141414` · blanco `#e5e5e5` · olive `#626148` · sage `#a4aba0`
- **Regla:** monocolor — un solo fill para todos los paths
- **Archivos de imagen:** en `assets/logos/01. PRINCIPAL/` y `assets/logos/02. SECUNDARIO/` (formatos SVG, PNG, JPG).

### Kisma (personaje)
- **viewBox:** `0 0 1000 1000` (cuadrado)
- **Estructura:** blob body + outline + 2 ojos + 2 piernas
- **Versiones oficiales:** ver archivos en `assets/logos/03. PERSONAJE/` (formatos SVG, PNG, JPG).
- **Uso de Kisma:** Selecciona la variante correcta de la carpeta `03. PERSONAJE` según el contexto.

### Tipografías
- **Principal:** Chillax (200–700) — títulos, CTAs, branding
- **Secundaria:** Synonym (200–700) — cuerpo de texto, UI
- **Fuentes embebidas:** en `assets/fonts.css` (base64, listas para inyectar)
- **Detalles completos:** en `references/typography.md`

### Colores
- **16 tonos** en 4 familias: Olive · Earth · Sage · Neutral
- **Sistema:** todos desaturados — prohibidos colores saturados y negro/blanco puro
- **Variables CSS + combos pre-aprobados:** en `references/colors-and-ui.md`

---

## Colores principales (referencia rápida)

| Token | HEX | Uso |
|---|---|---|
| `--olive-900` | `#626148` | Fondo oscuro, botones CTA, publicidad |
| `--earth-300` | `#e1dacd` | Fondo principal de páginas |
| `--neutral-300` | `#e5e5e5` | Fondo claro, logo negativo |
| `--brand-black` | `#141414` | Logo positivo, texto principal |
| `--brand-white` | `#e5e5e5` | Logo negativo, texto sobre oscuro |
| `--sage-900` | `#a4aba0` | Acento verde, Kisma body variante |

---

## Combos de color pre-aprobados

| Nombre | Fondo | Texto | Acento | Uso |
|---|---|---|---|---|
| **Campo** | `#e1dacd` | `#141414` | `#626148` | Web, landing pages |
| **Bosque** | `#626148` | `#e5e5e5` | `#b4bab1` | Hero, publicidad |
| **Niebla** | `#e5e5e5` | `#141414` | `#7c7b67` | App UI, interfaces limpias |
| **Tierra** | `#ada796` | `#e5e5e5` | `#e1dacd` | Posts RRSS |
| **Salvia** | `#a4aba0` | `#141414` | `#626148` | Cards de servicios |

---

## Reglas críticas de marca

**Color:**
- ✅ Mínimo 2 familias de color en cada pieza
- ❌ Sin negro puro `#000000` ni blanco puro `#ffffff`
- ❌ Sin colores saturados ni fuera de la paleta oficial

**Logo:**
- ✅ Margen de seguridad = ~50% del alto total del logo en todos los lados
- ✅ Logo solo en colores aprobados sobre fondos aprobados
- ❌ Sin distorsión, rotación, efectos, sombras o gradientes

**Tipografía:**
- ✅ Chillax para títulos y CTAs — Synonym para cuerpo de texto
- ❌ No mezclarlas en la misma línea

**Kisma:**
- ✅ Onboarding, RRSS, empty states, publicidad
- ❌ No en documentos formales ni comunicaciones de crisis

---

## Voz de la marca (resumen)

Kismet habla como un terapeuta amigo: accesible, empático, profesional.  
**USA:** equilibrio · bienestar · acompañamiento · calma · proceso  
**EVITA:** trastorno · enfermo · cura · diagnóstico (en comunicación pública)

---

## Checklist antes de entregar cualquier pieza

- [ ] Fuentes Chillax/Synonym embebidas desde `assets/fonts.css`
- [ ] Solo colores de la paleta oficial (16 tonos + brand-black/white)
- [ ] Mínimo 2 familias de color mezcladas
- [ ] Sin `#000000` ni `#ffffff`
- [ ] Logo con margen de seguridad y sobre fondo aprobado
- [ ] Tipografía correcta: Chillax en títulos/CTAs, Synonym en cuerpo
- [ ] Formas con border-radius ≥ 12px
- [ ] Tono cercano, empático, profesional

---

## Archivos de referencia

| Archivo | Cuándo leerlo |
|---|---|
| `assets/fonts.css` | Siempre — contiene las 12 fuentes en base64 listas para inyectar |
| `assets/logos/` | Contiene los logotipos y personaje Kisma en SVG, PNG y JPG |
| `references/colors-and-ui.md` | Para colores, CSS variables, componentes UI |
| `references/typography.md` | Para jerarquía tipográfica detallada y ejemplos de código |
| `references/voice-and-applications.md` | Para tono de comunicación, Kisma, fotografía y aplicaciones específicas |
