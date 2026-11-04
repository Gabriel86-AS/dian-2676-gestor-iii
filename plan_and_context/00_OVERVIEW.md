# DIAN 2676 · Gestor III — Plan maestro (leer primero en cada sesión)

## Objetivo
Sitio de estudio estático (GitHub Pages) para la prueba escrita **DIAN 2676 (CNSC/Areandina)**, empleo **Gestor III, código 303, grado 03, nivel Profesional**, ficha **AF-LF-3005** (Res. DIAN 0067 del 11-abr-2024, MERF). Proceso **Administrativo y Financiero**, subproceso **Recursos administrativos, operación logística, compras y contratos**. Fuente: `manual/manual_de_funciones-gestor3_jiovani.pdf` (2 págs.).

- **OPEC:** pendiente (pedirla a la persona usuaria; no inventarla).
- **Fecha del examen:** se asume la misma de la convocatoria, domingo 8-nov-2026, 8:00 a. m.–1:00 p. m. Confirmar con la citación.
- Los ejes reales del examen los fija la CNSC; la ficha es la mejor aproximación disponible.

Proyecto copiado del sitio de Gestor I (`gabriel86-as/dian-2676-estudio`): el motor, el progreso y los simulacros se reutilizan tal cual. El plan original quedó en `plan_and_context/gestor1_referencia/` (formato del examen, PJS, Likert y ponderación siguen siendo válidos; ver `dian_2676_recursos/dian_material/00_GOA_datos_clave.md`).

## Restricciones (igual que Gestor I)
Sin backend ni paso de compilación; HTML + CSS + JS (módulos ES); contenido en JSON; español de Colombia; primero el celular; progreso en `localStorage` con exportar/importar; sin castigos gamificados. **Cada ítem cita su fuente legal; nunca inventar artículos, plazos ni cifras.**

Aislamiento del sitio de Gestor I (mismo dominio `gabriel86-as.github.io`): claves `dian2676g3:*` en `localStorage` y cachés `dian2676g3-*` en `sw.js`. No volver a usar `dian2676:`.

## Unidades (según la ficha AF-LF-3005)
| id | Tema | Fuentes principales | Prioridad | Estado |
|---|---|---|---|---|
| `contratacion` | Contratación pública: etapas, modalidades, plan anual de adquisiciones, supervisión | Ley 80/1993, Ley 1150/2007, Ley 1474/2011, D. 1082/2015 | 1 | por hacer |
| `custodia-mercancias` | Custodia y disposición de mercancías aprehendidas, decomisadas o abandonadas; bienes adjudicados en cobro coactivo y procesos concursales | D. 1165/2019 (disposición de mercancías), procedimientos DIAN | 1 | por hacer |
| `ingreso-mercancias` | Control de ingresos, almacenamiento y registro de mercancías | D. 1165/2019, procedimientos DIAN | 1 | por hacer |
| `procedimiento-administrativo` | Ley 1437/2011 Títulos I, II y III (caps. I y V–VIII): notificaciones, recursos, actos administrativos | Ley 1437/2011, Ley 1755/2015 | 1 | por hacer |
| `servicios-infraestructura` | Servicios generales, infraestructura, inventarios y parque automotor | normas de bienes del Estado, procedimientos DIAN | 2 | por hacer |
| `siif` | Operación del SIIF Nación II | D. 1068/2015 (SIIF), guías MinHacienda | 2 | por hacer |
| `gestion-documental` | Gestión documental e instrumentos archivísticos | Ley 594/2000, AGN 001/2024 (en el paquete) | 2 | heredada de Gestor I; revisar enfoque |
| `constitucion-funcion-publica` | Derechos fundamentales, principios y estructura del Estado; principios de la función pública | Constitución Política, Ley 909/2004 | 2 | por hacer |
| `servicio-ciudadano` | Sistema PQRSF y políticas de servicio al ciudadano | Ley 1755/2015, Ley 1437/2011, CONPES/MIPG | 2 | por hacer |
| `transparencia-mipg` | Ley de transparencia, Código de Buen Gobierno, MIPG | Ley 1712/2014, D. 1083/2015 (MIPG, D. 1499/2017) | 3 | por hacer |
| `evasion-contrabando` | Conceptos de evasión, elusión y contrabando | Código Penal, Ley 1762/2015, ET | 3 | por hacer |
| `estructura` | Estructura de la DIAN | D. 1742/2020 (en el paquete) | 3 | heredada |
| `misionalidad` | Misionalidad de la DIAN | PEI 2024–2026 (en el paquete) | 3 | heredada |
| `razonamiento` | Razonamiento analítico | Saber Pro (en el paquete) | 3 | heredada |
| `comportamentales` | Comportamiento ético N4, Adaptabilidad N4, Innovación N3, Solución de problemas N4 (+ básicas comunes) | Res. DIAN 065/2024 | 3 | heredada; **reescribir con estos niveles** |
| `integridad` | Código de Integridad | Res. 065/2024, código general | 3 | heredada |

Las unidades tributarias de Gestor I (fiscalización, sanciones, obligaciones, liquidación, lavado, cambiaria, auditoría) se quitaron: no están en la ficha.

## Fuentes que faltan en el paquete
El paquete `dian_2676_recursos/` es de Gestor I. Antes de escribir cada unidad nueva, descargar el texto oficial (Secretaría del Senado, Función Pública – Gestor Normativo, Colombia Compra Eficiente, DIAN) a `dian_2676_recursos/gestor3/` (gitignored), y citar solo artículos verificados en ese texto.

## Fases
| # | Trabajo | Estado |
|---|---|---|
| 1 | Copia del repo, aislamiento de almacenamiento, rebranding, manifiesto nuevo | hecha |
| 2 | Fuentes faltantes + unidades de prioridad 1 | pendiente |
| 3 | Unidades de prioridad 2 | pendiente |
| 4 | Prioridad 3 + reescritura de `comportamentales` con los niveles de la ficha | pendiente |
| 5 | Regenerar simulacros (`node tools/build-tests.mjs`), auditoría de hechos, QA, publicación | pendiente |

Publicar al final de cada fase (`git push`).

## Protocolo de sesión
1. Leer este archivo y `current_state.md`; `content/SCHEMA.md` si se toca contenido.
2. `node tools/validate.mjs` antes de cada commit de contenido; quitar `"pending": true` al crear la unidad.
3. Si cambia el banco: `node tools/build-tests.mjs`. Si cambia el shell: subir `VERSION` en `sw.js`.
4. Commit, push y anotar 3–5 líneas en `plan/PROGRESS_LOG.md`; actualizar `current_state.md`.
