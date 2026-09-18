# Marco Normativo — Kismet

Este archivo documenta el marco normativo que sustenta las decisiones de producto, datos, pagos y cumplimiento de Kismet: un marketplace de salud emocional que conecta pacientes con un pool de psicólogos, agenda y cobra la sesión, y paga semanalmente al especialista descontando su fee de solución digital y cargos administrativos.

Cada norma incluye su alcance, aplicabilidad a Kismet, y la fuente de consulta. Cuando no existe sustento normativo directo, se indica como tal — no se fuerza una cita donde no la hay.

## Salud y telesalud

### Ley General de Salud (LGS) — Art. 32 Bis y Art. 72
- **Alcance**: define la telesalud/telemedicina como prestación de servicios de salud a distancia mediante TIC; el Art. 72 permite la atención médica a distancia siempre que se sigan las NOM aplicables.
- **Aplicación a Kismet**: fundamenta que la teleterapia prestada por los psicólogos de la red es una modalidad reconocida, sujeta a las NOM de expediente clínico e interoperabilidad.
- **Fuente**: [Ley General de Salud — Cámara de Diputados](https://www.diputados.gob.mx/LeyesBiblio/pdf/LGS.pdf); [Requisitos legales para telemedicina en México — Medesk](https://www.medesk.net/es/blog/requisitos-legales-para-telemedicina-en-mexico/)

### Reforma "Salud Digital" a la LGS (DOF, 15 de enero de 2026)
- **Alcance**: reordena la rectoría sanitaria y formaliza la salud digital; exige personal designado y capacitado, sistemas seguros y confiables, consentimiento informado que garantice comprensión y voluntariedad, y documentación/registro adecuados de la atención remota.
- **Aplicación a Kismet**: es el antecedente regulatorio más reciente y directo sobre plataformas de salud digital en México — cualquier feature de producto que toque agenda, videollamada o expediente debe poder demostrar estos cuatro elementos.
- **Fuente**: [Diario Oficial de la Federación, 15-ene-2026](https://dof.gob.mx/2026/PRESREP/PRESREP_150126_02.pdf); [Reforma a la Ley General de Salud — ConsultorSalud](https://consultorsalud.com.mx/reforma-ley-general-de-salud-mexico/)

### NOM-004-SSA3-2012 — Del expediente clínico
- **Alcance**: elementos mínimos, plazos de conservación y responsabilidad del profesional de salud sobre el expediente clínico, aplicable a todo acto médico incluida la consulta virtual.
- **Aplicación a Kismet**: cualquier registro de sesión, nota clínica o historial que la plataforma almacene en nombre del psicólogo debe cumplir estos elementos mínimos.
- **Fuente**: [Requisitos legales para telemedicina en México — Medesk](https://www.medesk.net/es/blog/requisitos-legales-para-telemedicina-en-mexico/)

### NOM-024-SSA3-2012 — Sistemas de información de registro electrónico para la salud. Intercambio de información
- **Alcance**: estándares de interoperabilidad, seguridad de datos e infraestructura para sistemas de expediente clínico electrónico.
- **Aplicación a Kismet**: relevante si el producto construye o integra un expediente clínico electrónico propio para las sesiones de psicoterapia.
- **Fuente**: [DOF-30NOV12-NOM-024-SSA3-2012 — DGIS Salud](http://www.dgis.salud.gob.mx/descargas/normatividad/normas/DOF-30NOV12-NOM-024-SSA3-2012.pdf)

### Aviso de Funcionamiento / COFEPRIS
- **Alcance**: los establecimientos de salud y prestadores de servicios de atención médica a distancia tramitan un Aviso de Funcionamiento (portal SICITEC), designando a un profesional de la salud responsable.
- **Aplicación a Kismet**: **por verificar con asesoría regulatoria**. Kismet es la plataforma tecnológica, no el prestador del servicio de salud (ese rol lo tiene cada psicólogo con su propia cédula); esta skill no afirma que Kismet como sociedad requiera el Aviso, pero es el primer punto a resolver con un abogado sanitarista antes de escalar la red de psicólogos.
- **Fuente**: [Requisitos legales para telemedicina en México — Medesk](https://www.medesk.net/es/blog/requisitos-legales-para-telemedicina-en-mexico/)

## Ejercicio profesional

### Ley Reglamentaria del Art. 5° Constitucional + Art. 79 LGS — Cédula profesional
- **Alcance**: exige título profesional registrado y cédula profesional vigente (Dirección General de Profesiones, SEP) para ejercer una profesión regulada, incluida la psicología.
- **Aplicación a Kismet**: requisito no negociable para dar de alta a un psicólogo en el pool. La cédula es pública y verificable en `cedulaprofesional.sep.gob.mx` — el flujo de onboarding de especialistas debe incluir esta verificación.
- **Fuente**: [Ley Reglamentaria del Artículo 5° Constitucional — Diputados](https://www.diputados.gob.mx/LeyesBiblio/pdf/208_190118.pdf); [Mental Health Licensing & Regulation in Mexico — TherapyRoute](https://www.therapyroute.com/article/mental-health-licensing-regulation-in-mexico-2025-guide-by-therapyroute)
- **Nota**: un psicólogo (no psiquiatra) no puede prescribir medicamentos; si Kismet en algún momento incorpora psiquiatría, este punto normativo cambia.

## Protección de datos

### LFPDPPP y su Reglamento — Art. 3, fracc. VI (datos personales sensibles)
- **Alcance**: los datos de salud —incluida la información psicológica que surge de una sesión de terapia— son datos personales sensibles. Su tratamiento exige consentimiento expreso y por escrito (firma autógrafa, huella o mecanismo equivalente), específico, informado e inequívoco, más aviso de privacidad y derechos ARCO.
- **Aplicación a Kismet**: cubre tanto los datos clínicos de los pacientes como cualquier nota o registro que el psicólogo capture en la plataforma. El consentimiento debe pedirse por cada finalidad (agenda, cobro, uso clínico, uso analítico/producto) y Kismet carga con la prueba de haberlo obtenido.
- **Fuente**: [Ley Federal de Protección de Datos Personales en Posesión de los Particulares — Diputados](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFPDPPP.pdf); [La protección de datos personales en los expedientes clínicos — IAPP](https://iapp.org/news/a/la-proteccion-de-datos-personales-en-los-expedientes-clinicos)

## Seguridad de la información

### ISO 13131:2021 — Health informatics — Telehealth services — Quality planning guidelines
- **Alcance**: guía internacional para planear la calidad de servicios de telesalud: seguridad del paciente, del prestador y de la transmisión de información.
- **Aplicación a Kismet**: marco de referencia directo para diseñar el flujo de teleterapia (agenda → sesión → registro), aun sin ser obligatorio por ley mexicana.
- **Fuente**: [ISO 13131:2021 — ISO.org](https://www.iso.org/standard/75962.html)

### ISO/IEC 27799 — Information security management in health using ISO/IEC 27002
- **Alcance**: controles de seguridad de la información específicos para el sector salud, construidos sobre ISO/IEC 27002.
- **Aplicación a Kismet**: referencia de buena práctica para proteger la infraestructura donde viven expedientes, notas de sesión y datos de pago.
- **Fuente**: [ISO 27799 — ISO.org](https://www.iso.org/standard/62777.html)

## Pagos

### PCI-DSS (estándar internacional de la industria de tarjetas, no gubernamental)
- **Alcance**: seguridad del manejo de datos de tarjeta de pago.
- **Aplicación a Kismet**: recomendación de buena práctica — delegar el alcance de cumplimiento PCI a un procesador de pagos certificado (Stripe, Conekta, MercadoPago, etc.) y operar Kismet bajo el cuestionario simplificado SAQ-A, evitando que la plataforma toque o almacene datos completos de tarjeta.
- **Fuente**: criterio de experiencia profesional / estándar de la industria — no se identificó una norma mexicana equivalente al momento de escribir esta skill.

## Laboral y societario

### REPSE — Registro de Prestadoras de Servicios Especializados (reforma LFT 2021, Art. 12-15)
- **Alcance**: obliga a registrarse a las empresas que ponen personal propio a disposición de un tercero para ejecutar servicios u obras especializadas que no son el objeto social del contratante.
- **Aplicación a Kismet**: análisis preliminar indica que **no aplica de forma directa** — los psicólogos son profesionales independientes, no personal de Kismet puesto a disposición de terceros, y la intermediación es el giro nuclear (no accesorio) del negocio. Sin embargo, es un punto de vigilancia legal: si el control operativo sobre los psicólogos aumenta (horarios fijos, exclusividad, supervisión directa), el riesgo de subordinación y por tanto de relación laboral encubierta crece. Validar con asesoría fiscal/laboral antes de escalar el modelo de contratación.
- **Fuente**: [REPSE: qué es, cómo registrarse y a quién aplica — Sofía Salud](https://www.sofiasalud.com/blog/repse-que-es); [Guía REPSE — STPS](https://repse.stps.gob.mx/assets/GUIA_REPSE.pdf)

## NMX

No se identificó una Norma Mexicana (NMX) vigente y específica para plataformas de telesalud o marketplaces de servicios psicológicos al momento de escribir esta skill (septiembre 2026). Si el usuario conoce una NMX aplicable, agréguese aquí con su fuente.

## Cómo usar este archivo

- Cita la norma específica (nombre + artículo/cláusula) al fundamentar una decisión — nunca solo "hay una norma que dice...".
- Si una recomendación no tiene sustento normativo directo, dilo explícitamente como "recomendación de buena práctica" o "criterio de experiencia profesional".
- Este marco es un punto de partida de investigación, no asesoría legal. Las aplicaciones marcadas "por verificar" requieren confirmación de un abogado especializado en salud digital / derecho corporativo antes de tomarse como definitivas.
