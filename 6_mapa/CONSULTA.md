# Índice del repo (memoria del agente)

Se consulta **antes** de preguntarle algo a Eric y **antes** de decir que algo falta, no existe o no está decidido.
Dice qué hay y en qué línea; lo que vale es siempre el archivo señalado. Se regenera con
`6_mapa/herramientas/indice_consulta.py`.

| Duda | Dónde mirar |
|---|---|
| Instrucciones de trabajo | `CLAUDE.md`; `.claude/rules/DECISIONES.md` (§2 de este índice) |
| ¿Eric ya decidió esto? | §2: cada decisión con archivo y línea |
| Qué falta y quién lo resuelve | `PENDIENTES.md` (§3) |
| Texto original de una regla | `2_corpus/…sqlite`, tabla `textos`, por `id` (INV-xxxxxx). Secciones de un documento: `SELECT DISTINCT encabezado FROM textos WHERE archivo=?` |
| Qué documentos tiene el corpus | §4 |
| Taxonomía, templates y casos | §1, carpetas `3_taxonomia/` y `4_diseno/` |


## 1. Archivos del repo (0)


## 2. Decisiones e instrucciones de Eric (archivo y línea)


**`CLAUDE.md`**

- L3 **Alcance y vocabulario de los prompts**
- L8 **Antes de decir que algo no existe**
- L16 **Consultar el mapa antes de preguntar o de dar algo por faltante (instrucción de Eric, 202…**
- L25 **Riesgos, pendientes y avance de etapa (decisión de Eric, 2026-10-29)**
- L35 **Toda lectura deja registro en el repo**
- L42 **Basura, auditorías y registro de cambios (instrucción de Eric, 2026-10-30)**

**`.claude/rules/DECISIONES.md`**

- L8 | 3 | Bloque de identidad con referencia de persona adjunta | Por rol de la referencia. Keyframe de inicio o fin en imagen a video: no re-describir. …
- L9 | 4 | Taxonomía de la base de reglas | Caso ampliado con LUGAR, EDIF, ANIMAL, OBJ, MULTITUD, ENSAMBLE. Tarea por subproceso, E0.1 a POST.2 | Las 852 …
- L10 | 5 | Tarjeta de ancla en la base | Las nueve dimensiones D1 a D9 como facetas multivalor de cada regla | Una pasada de clasificación adicional sobre…
- L11 | 6 | Modelo de embeddings | `intfloat/multilingual-e5-large` local, sin API key; la tabla admite añadir OpenAI después | Cubre inglés, español y rus…
- L12 | 8 | Cómo entran las inferencias | Con etiqueta `[A PRUEBA]`; investigación de campo en foros y tutoriales para confirmar o refutar cada una; un eje…
- L13 | 9 | Quién clasifica | Clasificador de dos capas, determinista por ruta y regex más similitud vectorial con confianza, y auditoría de Eric en hoja x…
- L15 **Principios que salieron de la sesión y quedan como reglas de trabajo**
- L23 **Cambios**

**`5_decisiones/01021_DECISIONES_APLICADAS_20261011_224300.md`**

- L15 **Decisión explícita de las 16:56:54.532502 UTC**
- L19 **Verificación documental y límites de capacidad**
- L23 **Cierre del trabajo de candidatas**

**`5_decisiones/01022_DELTA_DECISIONES_CONSOLIDADO_20261011_224300.md`**

- L3 **Estado y autorización**
- L11 **Cambios del contrato**
- L28 **Jerarquías y estados**
- L34 **DEC-000026 y DEC-000027: evidencia disponible y límite**
- L42 **Registro histórico recibido**
- L46 **DEC-000001**
- L53 **DEC-000002**
- L59 **DEC-000003**
- L65 **DEC-000004**
- L71 **DEC-000005**
- L78 **DEC-000006**
- L84 **DEC-000007**
- L90 **DEC-000008**
- L96 **DEC-000009**
- L102 **DEC-000010**
- L108 **DEC-000011**
- L114 **DEC-000012**
- L121 **DEC-000013**
- L127 **DEC-000014**
- L133 **DEC-000015**
- L139 **DEC-000016**
- L145 **DEC-000017**
- L151 **DEC-000018**
- L157 **DEC-000019**
- L164 **DEC-000020**
- L171 **DEC-000021**
- L178 **DEC-000022**
- L184 **DEC-000023**
- L192 **DEC-000024**
- L198 **DEC-000025**
- L205 **Decisión adicional explícita: anclas/keyframes, 2026-10-11 16:56:54.532502 UTC**
- L216 **Cierre de verificación documental, sin inventar rendimiento actual**
- L224 **Resultado de aplicación de la decisión de anclas/keyframes**

**`5_decisiones/01062_registro_decisiones_DOC01.md`**

- L4 **DEC-000001**
- L8 **DEC-000002**
- L11 **DEC-000003**
- L14 **DEC-000004**
- L17 **DEC-000005**
- L21 **DEC-000006**
- L24 **DEC-000007**
- L27 **DEC-000008**
- L30 **DEC-000009**
- L33 **DEC-000010**
- L36 **DEC-000011**
- L39 **DEC-000012**
- L43 **DEC-000013**
- L46 **DEC-000014**
- L49 **DEC-000015**
- L52 **DEC-000016**
- L55 **DEC-000017**
- L58 **DEC-000018**
- L61 **DEC-000019**
- L65 **DEC-000020**
- L69 **DEC-000021**
- L73 **DEC-000022**
- L76 **DEC-000023**
- L81 **DEC-000024**
- L84 **DEC-000025**

**`5_decisiones/DECISIONES_ERIC_20261023.md`**

- L3 1. Alcance de esta fase: solo textos de imagen y GPT Image 2. Universo: los 1,511 textos de `skills/image/**`
- L7 2. La catalogación previa (2026-10-11, 1,887 registros) y la catalogación provisional del 2026-10-23 no se
- L9 3. Ningún texto queda como pendiente, propuesta, duda, NO APLICA ni equivalente. Lo que no cabe en la taxonomía se
- L11 4. Extensiones de la taxonomía aprobadas (se registran aparte de la taxonomía original):
- L29 5. Toda etiqueta usada en la catalogación debe coincidir al 100% con la taxonomía original (o con una extensión
- L31 6. Las pruebas se hacen solo con GPT Image 2; otros modelos se añaden después.
- L32 7. quality en GPT Image 2 (consulta C1 del piloto): la elige el usuario; «medium como punto de partida» y «empieza con
- L34 8. Biblioteca de prompts efectivos (precisada por Eric el 2026-10-23):

**`5_decisiones/DECISIONES_ERIC_20261024.md`**

- L7 1. **Alcance del universo de textos** (amplía la decisión 1 de `DECISIONES_ERIC_20261023.md` y responde D2 del plan v3
- L19 2. «SI EXISTE LA CLASIFICACIÓN EN LA TAXONOMÍA ES PORQUE LA REGLA EXISTE EN EL CORPUS».
- L20 3. «EL SOLO HACER LA GENERACIÓN EN DOS PASOS NO ES SUFICIENTE, HAY VARIAS REGLAS MUY ESPECÍFICAS SOBRE EL LENTE Y EL
- L23 4. Método de prueba aprobado el 2026-10-24: bloque armado por casos (universo completo → filtro por caso → controles

**`5_decisiones/DECISIONES_ERIC_20261026.md`**

- L5 1. **Cuando un texto da una cifra que no es la de GPT Image 2, vale la cifra que el corpus da para GPT Image 2**, y el
- L13 2. «No estás aprobado para asumir nada, siempre lo verificas»: toda afirmación sobre un texto se comprueba leyendo el
- L15 3. «Siempre que hay una supuesta contradicción o incoherencia tienes que leer exhaustivamente los textos
- L18 4. **Interfaces de GPT Image 2: OpenAI API y fal.ai** (respuesta a la decisión 1 de 6). Manda
- L23 5. **F20 con una sola persona que debe seguir reconocible: «todas»** (decisión 2 de 6). Base: TRM-0175 (taxonomía L1220,
- L26 6. **Extensión F24 + «objeto entero»** (decisión 3 de 6): un objeto completo como sujeto del cuadro. Los 8 valores
- L29 7. **F05 de B1 y B4 deja de ser lista vacía** (decisión 4 de 6; la lista vacía viola taxonomía §1.12.8): B1 (pescadora en
- L32 8. **Interfaz de generación de la prueba: App de ChatGPT para escritorio** (corregido 2026-10-27). Palabras de Eric:
- L37 9. **Muestra de auditoría** (2026-10-27): Eric revisa al azar el 10 % del total de reglas marcadas «no aplica» en cada
- L40 10. **Repetición antes de auditar** (2026-10-27): si una imagen sale mal, se genera el mismo prompt por lo menos dos veces
- L45 11. **Longitud del prompt** (2026-10-27): ya estaba decidida (`.claude/rules/DECISIONES.md` decisión 2; T-BRIEF-IMG L355).
- L49 12. **Alcance de la prueba: solo imagen con aspecto de foto real** (2026-10-27). Palabras de Eric: «solo quiero que se
- L57 13. **vision-decomposer y transferencia de estilo son cosas distintas** (2026-10-27). Palabras de Eric: «porque si son
- L62 14. **Caso de descripción de imagen** (2026-10-27).
- L70 15. **Sin veredicto d en el diagnóstico** (2026-10-27, responde la pregunta 3). Palabras de Eric: «no hay límite de
- L76 16. **Lista de casos de la prueba** (2026-10-27). Eric
- L85 17. **Boceto o plano a final: 5 casos** (2026-10-27). Eric eligió un caso por cada plantilla fotográfica, igual que en
- L94 18. **Dos textos mal excluidos entran al universo** (2026-10-27). Eric respondió «Sí, meterlos» a la pregunta «¿Meto
- L103 19. **La decisión por sección se mantiene** (2026-10-27, 00:28–00:37 UTC; registrada tarde, el 2026-10-27). Se decidió en

**`5_decisiones/DECISIONES_ERIC_20261027_30.md`**

- L7 1. **Objetivo y reparto** (2026-10-27): «EL SISTEMA NO GENERA IMÁGENES, GENERA PROMPTS Y YO HAGO LAS IMÁGENES». El
- L9 2. **Qué se queda en el repo** (2026-10-27): «LOS ARCHIVOS QUE SE QUEDAN SON LOS QUE NECESITAS PARA EL SISTEMA ENTERO,
- L11 3. **No repetir preguntas ya respondidas** (2026-10-27): no volver a preguntar lo que Eric ya contestó en conversaciones
- L13 4. **Planes** (2026-10-27): un plan tiene como máximo 10 pasos, extremadamente claros y sin riesgos sin mitigar.
- L14 5. **Riesgos y pendientes** (2026-10-29): registrado en CLAUDE.md, sección «Riesgos, pendientes y avance de etapa».
- L15 6. **Procedimiento para terminar** (2026-10-29, palabras de Eric resumidas punto por punto):
- L16 1. Una estructura clara de la aplicación que va a gobernar y ejecutar el sistema, con un flujo claro de la
- L18 2. Los textos se clasifican primero por tipo de texto. La primera clasificación es si tienen o no impacto en la
- L23 3. Para todos los textos debe existir de qué documento viene y su taxonomía dentro de ese documento: los
- L25 4. Una tabla con el ID de cada texto en la primera columna y, en las siguientes, todas las columnas que
- L27 5. La primera ronda de catálogo es mecánica: usa el documento y los encabezados a los que pertenece el texto.
- L28 6. La segunda ronda revisa los textos, una categoría por vez, no todas al mismo tiempo.
- L29 7. La matriz lleva X si aplica para esa categoría y 0 si no; al final todas las celdas deben estar llenas.
- L33 7. **Auditoría con prueba** (2026-10-29): Eric pidió auditar 100 textos corregidos y traer prueba de que están
- L35 8. **Nada sin verificar** (2026-10-30): «no me des una aseveración que no has verificado personalmente». Toda
- L38 9. **Para qué es el mapa** (2026-10-30): el mapa es para que el agente lo consulte y no pierda la memoria de las
- L42 11. **Borrar de forma irrecuperable** (2026-10-30): «cuando digo bórralos no es para que los escondas en algún archivo
- L45 12. **Repo, hooks y mapa** (2026-10-30, segunda parte):
- L64 13. **Basura, auditorías y registro de cambios** (2026-10-30): borrar siempre los archivos basura que se generen; una
- L68 14. **Ninguna referencia a documentos borrados** (2026-10-30): se borran todos los documentos que Eric ordenó borrar y toda

**`5_decisiones/DECISIONES_ERIC_20261031.md`**

- L3 1. **Sin categoría «dato libre del caso»** (2026-10-31): «ESTÁ PROHIBIDA ESA CATEGORÍA LIBRE DE CASO, LA TRADUCCIÓN VA
- L7 2. **Valores nuevos de la taxonomía** (2026-10-31): «OK ADELANTE CON TU RECOMENDACIÓN». Aprobada la recomendación de la
- L10 3. **Nueva taxonomía canónica** (2026-10-31): «GUARDA EL CAMBIO EN EL LOG CON LO QUE QUEDA MODIFICADA MI DECISIÓN SOBRE
- L16 4. **Aporte de Eric: biomecánica del galope** (2026-10-31), tras ver que el prompt del piloto produjo un caballo al trote.
- L34 5. **Copias idénticas** (2026-10-31): «COPIA IDÉNTICA SE CLASIFICA LAS VECES QUE SEA NECESARIA PORQUE UNA MISMA REGLA PUEDE
- L37 6. **Herramienta de investigación del movimiento y bloque «Acción»** (2026-10-31): «TENEMOS QUE AGREGAR UNA HERRAMIENTA Y UN
- L43 7. **Cómo se resuelven las dudas al clasificar** (2026-10-31): «LAS DUDAS SE RESUELVEN DOS NIVELES DE JERARQUÍA DE
- L51 8. **Respuestas de Eric a los hallazgos del piloto** (2026-10-31), literal: «REVISA EL UNIVERSO EXHAUSTIVAMENTE, OBVIAMENTE HAY

**`5_decisiones/DECISIONES_ERIC_RESCATADAS_20261027.md`**

- L5 **De la app anterior (2026-09-28)**
- L10 **Directivas del 21 y 22 de octubre (hoy en `5_decisiones/directivas_20261021/`)**

**`5_decisiones/DECISIONES_repo_20260925.md`**

- L8 | 3 | Bloque de identidad con referencia de persona adjunta | Por rol de la referencia. Keyframe de inicio o fin en imagen a video: no re-describir. …
- L9 | 4 | Taxonomía de la base de reglas | Caso ampliado con LUGAR, EDIF, ANIMAL, OBJ, MULTITUD, ENSAMBLE. Tarea por subproceso, E0.1 a POST.2 | Las 852 …
- L10 | 5 | Tarjeta de ancla en la base | Las nueve dimensiones D1 a D9 como facetas multivalor de cada regla | Una pasada de clasificación adicional sobre…
- L11 | 6 | Modelo de embeddings | `intfloat/multilingual-e5-large` local, sin API key; la tabla admite añadir OpenAI después | Cubre inglés, español y rus…
- L12 | 8 | Cómo entran las inferencias | Con etiqueta `[A PRUEBA]`; investigación de campo en foros y tutoriales para confirmar o refutar cada una; un eje…
- L13 | 9 | Quién clasifica | Clasificador de dos capas, determinista por ruta y regex más similitud vectorial con confianza, y auditoría de Eric en hoja x…
- L15 **Principios que salieron de la sesión y quedan como reglas de trabajo**
- L23 **Cambios**

**`5_decisiones/directivas_20261021/directivas_taller.json`**

- `ERIC-IDIOMA-PROMPT-INGLES`: «en ingles esto es siemore»
- `ERIC-BLOQUES-1-2-NO-TOPE`: «La expectativa de una o dos reglas por bloque sirve para evaluar los filtros, no para imponer un tope ni excluir reglas válidas.»

**`5_decisiones/directivas_20261021/user_directives.json`**

- `ERIC-B1-PHOTOREALISTIC`: «Prohibido el término photorealistic en prompts»
- `ERIC-DELEGATION-TERMS`: «Se perdió la prohibición explícita del usuario de photorealistic y fotorealista.»

## 3. Pendientes (`PENDIENTES.md`)

- L14 **P-17** (Eric; Cerrado 2026-10-30: restaurados por orden de Eric…): Hooks del paquete original
- L15 **P-18** (Eric, con el agente; Abierto): Revisar con Eric los archivos del zip que no están en `skills/` antes de decidir qué se borra
- L16 **P-05** (Eric; Abierto): Aprobación del índice `6_mapa/CONSULTA.md`
- L22 **P-06** (Agente, con aprobación de Eric; Abierto): Incorporar las extensiones de la taxonomía del 23 y del 26 de octubre (F32–F35 y valores nuevos en F04, F05, F06, F10, …
- L23 **P-07** (Agente propone, Eric aprueba; Abierto): Mecanismo para clasificar sin perder el estado: cómo retoma el trabajo un agente cuya conversación se compacta a mitad …
- L24 **P-08** (Eric; Abierto): `text-rendering.md`: Nano Banana con más de 100 idiomas (INV-003296); en la sección «Multilingual / Localization», sin …
- L25 **P-09** (Eric; Abierto): `screenwriter/SKILL.md`: 8–15 escenas (INV-003470) frente a 6–10 para 5 minutos (INV-003574)
- L26 **P-10** (Eric; Abierto): Seedream y el texto: `_capabilities.json` frente a su adaptador
- L27 **P-11** (Eric; Abierto): `validate_prompts.py`: la regla del tercio lleva `or True` (INV-012830)
- L28 **P-12** (Eric; Abierto): `patterns-and-genres.md` (7 o 8 géneros) y `shot-grammar.md` (`rack`)
- L29 **P-13** (Eric; Abierto): Tope de costo de la clasificación
- L30 **P-19** (Agente, con aprobación de Eric; Abierto): Regenerar el catálogo de casos (`4_diseno/casos/`) desde la taxonomía canónica; hoy `build_catalog.py` lo construye des…
- L31 **P-20** (Eric; Abierto): Qué se hace con la taxonomía anterior 00688, que dejó de ser canónica y sigue en `3_taxonomia/`
- L32 **P-21** (Eric; Abierto): Criterios centralizados de clasificación (`4_diseno/CRITERIOS_CLASIFICACION.md`)
- L33 **P-22** (Eric; Cerrado 2026-10-31: Eric indica que el universo t…): Ampliar el universo de la fase con `flujos/flujo-anclas.html` y `skills/visual-media/SKILL.md`, donde están las reglas …
- L34 **P-23** (Eric; Cerrado 2026-10-31: high; extra high para imágene…): Calidad de GPT Image 2: medium por defecto, empezar en low, high para fotorrealismo, high en hero (piloto, H2)
- L35 **P-24** (Eric; Cerrado 2026-10-31: es «imagen fija suelta» del c…): F04 sin tipo para una foto suelta; el slot Use Case lo necesita (piloto, H3)
- L36 **P-25** (Eric; Cerrado 2026-10-31: F20, F21 y F22 valen igual pa…): F20 a F22 son de personas y no tienen valor para un sujeto animal (piloto, H4)
- L37 **P-26** (Eric; Cerrado 2026-10-31: atardecer ya existe y equival…): Definiciones de hora dorada y atardecer (piloto, H5)
- L38 **P-27** (Agente; Cerrado 2026-10-31: revisados los 206 documentos;…): Precatalogación: las secciones de primer nivel de `skills/image/SKILL.md` quedaron en «texto antes del primer encabezad…
- L39 **P-28** (Eric; Cerrado 2026-10-31: lo cubre la decisión 6 (herra…): Que el aporte de Eric sobre la biomecánica del galope (decisiones del 31-oct, punto 4) entre como regla (piloto, H8)
- L40 **P-29** (Eric; Abierto): Definición de «muy sofisticada» en F37 Grado de dificultad: escena compleja, bloque «Acción», texto extenso o pequeño, …
- L41 **P-30** (Agente; Abierto): Relectura exhaustiva del universo para el caso caballo con el criterio corregido (una regla en la plantilla de otra pie…

## 4. Corpus: 206 archivos, 141 contenidos distintos, 13,003 textos

Por skill: sus documentos (ruta dentro de la skill). Utilidad ALTA salvo que diga [MEDIA] (regula el proceso) o [NULA] (ni una ni otra). «= x» marca una copia idéntica de x. Textos, ids y secciones de un documento: `SELECT id, encabezado, linea_inicial FROM textos WHERE archivo=?`.

- **flujos** (2 archivos, 612 textos): flujo-anclas.html; flujo-spot.html
- **ai-production-director** (3 archivos, 162 textos): SKILL.md; references/creative-strategy.md [MEDIA]; references/production-package.md
- **ai-video-storyboard** (2 archivos, 165 textos): SKILL.md; examples/tiktok-reel-30s-coffee.md
- **brand-lock-extractor** (23 archivos, 970 textos): LICENSE [NULA]; SKILL.md [MEDIA]; brand-packs/README.md [MEDIA]; brand-packs/_template.md; brand-packs/examples/saas-clean.md; examples/brand-lock.md; examples/input-brief.md; references/extraction-rubric.md; templates/brand-lock.md.tpl; tools/README.md; tools/_shotkit.py [MEDIA]; tools/_template.py [NULA]; tools/check.sh [MEDIA]; tools/copy-prompt.py [MEDIA]; tools/shots-to-html.py [MEDIA]; tools/validate_brand_lock.py [MEDIA]; tools/validate_capabilities.py; tools/validate_critique.py [MEDIA]; tools/validate_prompts.py; tools/validate_provenance.py [MEDIA]; tools/validate_schemas.py [MEDIA]; tools/validate_shots.py [MEDIA]; tools/validate_skills.py [MEDIA]
- **image** (25 archivos, 1,548 textos): LICENSE [NULA]; NOTICE [NULA]; SKILL.md; references/characters.md; references/creative-direction.md; references/dimensional.md; references/editing.md; references/golden-rules.md; references/gpt-image.md; references/models.md; references/multi-panel.md; references/nano-banana.md; references/patterns/character-design.md; references/patterns/ecommerce.md; references/patterns/fashion-editorial.md; references/patterns/food-beverage.md; references/patterns/portrait-cinema.md; references/patterns/poster-illustration.md; references/patterns/ui-social.md; references/prompt-framework.md; references/slides.md; references/storyboards.md; references/structural.md; references/text-rendering.md; references/vision-decomposer.md
- **screenwriter** (3 archivos, 392 textos): SKILL.md [MEDIA]; references/advanced-techniques.md [MEDIA]; references/pipeline-integration.md [MEDIA]
- **storyboard-architect** (44 archivos, 3,119 textos): LICENSE = `skills/brand-lock-extractor/LICENSE`; SKILL.md; brand-packs/README.md = `skills/brand-lock-extractor/brand-packs/README.md`; brand-packs/_template.md = `skills/brand-lock-extractor/brand-packs/_template.md`; examples/30s-pain-proof-promise/brand-lock.snapshot.md; examples/30s-pain-proof-promise/preview.html; examples/30s-pain-proof-promise/run.json [MEDIA]; examples/30s-pain-proof-promise/shots.json; examples/30s-pain-proof-promise/storyboard.md; examples/30s-pain-proof-promise/text-overlays.json [MEDIA]; examples/60s-founder-explainer/brand-lock.snapshot.md = `skills/storyboard-architect/examples/30s-pain-proof-promise/brand-lock.snapshot.md`; examples/60s-founder-explainer/preview.html; examples/60s-founder-explainer/run.json [MEDIA]; examples/60s-founder-explainer/shots.json; examples/60s-founder-explainer/storyboard.md; examples/60s-founder-explainer/text-overlays.json [MEDIA]; examples/shotkit-explainer/brand-lock.snapshot.md; examples/shotkit-explainer/preview.html; examples/shotkit-explainer/run.json [MEDIA]; examples/shotkit-explainer/shots.json; examples/shotkit-explainer/storyboard.md; examples/shotkit-explainer/text-overlays.json [MEDIA]; references/beat-frameworks.md [MEDIA]; references/on-screen-text.md; references/shot-grammar.md; references/timing-rules.md [MEDIA]; templates/run.schema.json [MEDIA]; templates/shots.schema.json [MEDIA]; templates/storyboard.md.tpl [MEDIA]; templates/text-overlays.schema.json; tools/README.md = `skills/brand-lock-extractor/tools/README.md`; tools/_shotkit.py = `skills/brand-lock-extractor/tools/_shotkit.py`; tools/_template.py = `skills/brand-lock-extractor/tools/_template.py`; tools/check.sh = `skills/brand-lock-extractor/tools/check.sh`; tools/copy-prompt.py = `skills/brand-lock-extractor/tools/copy-prompt.py`; tools/shots-to-html.py = `skills/brand-lock-extractor/tools/shots-to-html.py`; tools/validate_brand_lock.py = `skills/brand-lock-extractor/tools/validate_brand_lock.py`; tools/validate_capabilities.py = `skills/brand-lock-extractor/tools/validate_capabilities.py`; tools/validate_critique.py = `skills/brand-lock-extractor/tools/validate_critique.py`; tools/validate_prompts.py = `skills/brand-lock-extractor/tools/validate_prompts.py`; tools/validate_provenance.py = `skills/brand-lock-extractor/tools/validate_provenance.py`; tools/validate_schemas.py = `skills/brand-lock-extractor/tools/validate_schemas.py`; tools/validate_shots.py = `skills/brand-lock-extractor/tools/validate_shots.py`; tools/validate_skills.py = `skills/brand-lock-extractor/tools/validate_skills.py`
- **storyboard-html-preview** (19 archivos, 843 textos): LICENSE = `skills/brand-lock-extractor/LICENSE`; SKILL.md [MEDIA]; templates/preview.html.tpl [MEDIA]; templates/print.css.tpl [MEDIA]; templates/styles.css.tpl [MEDIA]; tools/README.md = `skills/brand-lock-extractor/tools/README.md`; tools/_shotkit.py = `skills/brand-lock-extractor/tools/_shotkit.py`; tools/_template.py = `skills/brand-lock-extractor/tools/_template.py`; tools/check.sh = `skills/brand-lock-extractor/tools/check.sh`; tools/copy-prompt.py = `skills/brand-lock-extractor/tools/copy-prompt.py`; tools/shots-to-html.py = `skills/brand-lock-extractor/tools/shots-to-html.py`; tools/validate_brand_lock.py = `skills/brand-lock-extractor/tools/validate_brand_lock.py`; tools/validate_capabilities.py = `skills/brand-lock-extractor/tools/validate_capabilities.py`; tools/validate_critique.py = `skills/brand-lock-extractor/tools/validate_critique.py`; tools/validate_prompts.py = `skills/brand-lock-extractor/tools/validate_prompts.py`; tools/validate_provenance.py = `skills/brand-lock-extractor/tools/validate_provenance.py`; tools/validate_schemas.py = `skills/brand-lock-extractor/tools/validate_schemas.py`; tools/validate_shots.py = `skills/brand-lock-extractor/tools/validate_shots.py`; tools/validate_skills.py = `skills/brand-lock-extractor/tools/validate_skills.py`
- **video** (15 archivos, 1,918 textos): LICENSE = `skills/image/LICENSE`; NOTICE = `skills/image/NOTICE`; SKILL.md; references/animatic-keyframes.md; references/camera-lighting-vocabulary.md; references/dramaturgy.md; references/fixes-and-skeletons.md; references/kling.md; references/patterns-and-genres.md; references/race-and-speed.md; references/role-modes.md; references/seedance-25.md; references/seedance.md; references/universal-rules.md; references/veo.md
- **visual-asset-critic** (30 archivos, 1,417 textos): LICENSE = `skills/brand-lock-extractor/LICENSE`; SKILL.md; examples/critique.accept.json [MEDIA]; examples/critique.revise.json; examples/worked-run/brand-lock.snapshot.md = `skills/storyboard-architect/examples/30s-pain-proof-promise/brand-lock.snapshot.md`; examples/worked-run/critiques/round-1/shot_01.critique.json [MEDIA]; examples/worked-run/critiques/round-1/shot_02.critique.json; examples/worked-run/critiques/round-2/shot_02.critique.json [MEDIA]; examples/worked-run/preview.html [MEDIA]; examples/worked-run/prompts/round-1/flux.txt; examples/worked-run/prompts/round-2/revised-flux.txt; examples/worked-run/run.json [MEDIA]; examples/worked-run/shots.json [MEDIA]; examples/worked-run/text-overlays.json [MEDIA]; references/critique-rubric.md; templates/critique.schema.json [MEDIA]; tools/README.md = `skills/brand-lock-extractor/tools/README.md`; tools/_shotkit.py = `skills/brand-lock-extractor/tools/_shotkit.py`; tools/_template.py = `skills/brand-lock-extractor/tools/_template.py`; tools/check.sh = `skills/brand-lock-extractor/tools/check.sh`; tools/copy-prompt.py = `skills/brand-lock-extractor/tools/copy-prompt.py`; tools/shots-to-html.py = `skills/brand-lock-extractor/tools/shots-to-html.py`; tools/validate_brand_lock.py = `skills/brand-lock-extractor/tools/validate_brand_lock.py`; tools/validate_capabilities.py = `skills/brand-lock-extractor/tools/validate_capabilities.py`; tools/validate_critique.py = `skills/brand-lock-extractor/tools/validate_critique.py`; tools/validate_prompts.py = `skills/brand-lock-extractor/tools/validate_prompts.py`; tools/validate_provenance.py = `skills/brand-lock-extractor/tools/validate_provenance.py`; tools/validate_schemas.py = `skills/brand-lock-extractor/tools/validate_schemas.py`; tools/validate_shots.py = `skills/brand-lock-extractor/tools/validate_shots.py`; tools/validate_skills.py = `skills/brand-lock-extractor/tools/validate_skills.py`
- **visual-media** (1 archivos, 83 textos): SKILL.md [MEDIA]
- **visual-prompt-forge** (39 archivos, 1,774 textos): LICENSE = `skills/brand-lock-extractor/LICENSE`; SKILL.md; adapters/_capabilities.json; adapters/capabilities.schema.json [MEDIA]; adapters/flux.md; adapters/gpt-image.md; adapters/hailuo.md; adapters/ideogram.md; adapters/kling.md; adapters/midjourney.md; adapters/nano-banana.md; adapters/seedance.md; adapters/seedream.md; adapters/veo.md; examples/one-shot-all-adapters/README.md; examples/one-shot-all-adapters/flux.txt; examples/one-shot-all-adapters/gpt-image.txt; examples/one-shot-all-adapters/ideogram.txt; examples/one-shot-all-adapters/kling.txt; examples/one-shot-all-adapters/midjourney.txt; examples/one-shot-all-adapters/nano-banana.txt; examples/one-shot-all-adapters/seedream.txt; references/consistency-locks.md; references/failure-modes.md; references/prompt-anatomy.md; tools/README.md = `skills/brand-lock-extractor/tools/README.md`; tools/_shotkit.py = `skills/brand-lock-extractor/tools/_shotkit.py`; tools/_template.py = `skills/brand-lock-extractor/tools/_template.py`; tools/check.sh = `skills/brand-lock-extractor/tools/check.sh`; tools/copy-prompt.py = `skills/brand-lock-extractor/tools/copy-prompt.py`; tools/shots-to-html.py = `skills/brand-lock-extractor/tools/shots-to-html.py`; tools/validate_brand_lock.py = `skills/brand-lock-extractor/tools/validate_brand_lock.py`; tools/validate_capabilities.py = `skills/brand-lock-extractor/tools/validate_capabilities.py`; tools/validate_critique.py = `skills/brand-lock-extractor/tools/validate_critique.py`; tools/validate_prompts.py; tools/validate_provenance.py = `skills/brand-lock-extractor/tools/validate_provenance.py`; tools/validate_schemas.py = `skills/brand-lock-extractor/tools/validate_schemas.py`; tools/validate_shots.py = `skills/brand-lock-extractor/tools/validate_shots.py`; tools/validate_skills.py = `skills/brand-lock-extractor/tools/validate_skills.py`
