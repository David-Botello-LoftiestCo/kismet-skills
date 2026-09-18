# Directorio de Knowledge Bases — Notion de Kismet

Este archivo mapea los recursos del workspace de Notion de Kismet con sus IDs, para consulta directa. El workspace está en construcción: la estructura objetivo se documenta aquí desde ahora, y los IDs se completan conforme cada página o base de datos se crea.

**Antes de usar un ID marcado como `pendiente`**: usa `Notion:notion-search` para verificar si el recurso ya existe con otro nombre, y si no existe, dilo explícitamente al usuario en vez de inventar contenido.

## Página principal

- **KISMET | Main Page**: `pendiente`

## Knowledge bases normativas y de cumplimiento

### Marco normativo — Telesalud, datos y pagos
- **ID**: `pendiente`
- **Contenido**: versión viva de `references/marco-normativo.md` — norma por norma, con estado de cumplimiento y responsable
- **Cuándo consultar**: cualquier decisión de producto, legal o de cumplimiento; antes de escribir aviso de privacidad, consentimiento informado o contratos con psicólogos

### Consentimiento informado y avisos de privacidad
- **ID**: `pendiente`
- **Contenido**: plantillas vigentes de consentimiento informado, aviso de privacidad para pacientes y psicólogos
- **Cuándo consultar**: onboarding de pacientes o psicólogos, cambios de producto que toquen datos de salud

## Bases de datos operativas

### Catálogo de psicólogos / Red de especialistas
- **Database ID**: `pendiente`
- **Contenido**: especialistas dados de alta, especialidad, cédula profesional, disponibilidad, tarifa
- **Cuándo consultar**: alta de nuevos especialistas, matching paciente-psicólogo, capacidad de la red

### Costos operativos y split de pagos
- **Database ID**: `pendiente`
- **Contenido**: fee de Kismet por sesión, costos de procesamiento de pago, calendario de payouts semanales a psicólogos
- **Cuándo consultar**: pricing, análisis de rentabilidad, evaluación de viabilidad financiera

### Pipeline de pacientes / Adquisición
- **Database ID**: `pendiente`
- **Contenido**: segmentos objetivo, canales de adquisición, funnel de sign up a primera sesión
- **Cuándo consultar**: marketing, producto, análisis de conversión

### Equipo de trabajo
- **Database ID**: `pendiente`
- **Cuándo consultar**: asignación de tareas, seguimiento de equipo

## Páginas de contenido y marketing

### Brand Voice — Kismet
- **ID**: `pendiente`
- **Contenido**: personalidad de marca, tono, estilo de comunicación pública (complementa la skill `kismet-brand`)
- **Cuándo consultar**: creación de contenido para redes, definición de tono en comunicaciones públicas

## Páginas de gestión y gobierno corporativo

### Dirección de Portafolios
- **ID**: `pendiente`
- **Contenido**: vista general de todos los proyectos activos y en backlog
- **Cuándo consultar**: visión macro del estado de la firma, priorización de recursos

### Gobierno corporativo — Alta Dirección
- **ID**: `pendiente`
- **Contenido**: estructura societaria, actas, políticas internas, decisiones de dirección
- **Cuándo consultar**: temas de constitución de la sociedad, gobierno corporativo, decisiones de alta dirección

### Análisis Financiero
- **ID**: `pendiente`
- **Contenido**: estructura de costos, flujo de caja, proyecciones
- **Cuándo consultar**: evaluación financiera, pricing, cash flow projection

## Patrón de consulta recomendado

1. **Búsqueda semántica** → `Notion:notion-search` con query específica cuando no sabes dónde está la información o si el recurso ya existe
2. **Fetch directo** → `Notion:notion-fetch` con ID cuando ya lo conoces (una vez que este archivo se actualice con IDs reales)
3. **Búsqueda en data source** → `Notion:notion-search` con `data_source_url` cuando buscas dentro de una base de datos específica

Actualiza este archivo (reemplazando `pendiente` por el ID real) cada vez que se cree un recurso nuevo en el workspace de Kismet.
