# Current State (2026-11-04)

**Fase 1 hecha: copia del sitio de Gestor I adaptada a Gestor III.** Repo nuevo con historia limpia. Motor, progreso, repaso y simulacros funcionan igual.

- Almacenamiento aislado del sitio de Gestor I: claves `dian2676g3:*`, cachés `dian2676g3-*` (el `activate` de `sw.js` solo borra cachés propias).
- Manifiesto nuevo según la ficha AF-LF-3005: 16 unidades; 6 heredadas con contenido (`gestion-documental`, `estructura`, `misionalidad`, `razonamiento`, `comportamentales`, `integridad`) y 10 nuevas en `"pending": true`.
- Simulacros regenerados solo con las unidades heredadas (provisional).
- `node tools/validate.mjs` sin errores; `tests/progress.test.js` 14/14; `tests/simulacro.test.js` 9/9; E2E `qa-site` 23/23 (sin la prueba del aviso post-corte: ninguna unidad tiene ítems así), `simulacro-basico` 15/15, `simulacro-examen` 10/10.
- `manual/` (PDF de la ficha) está en `.gitignore`, igual que el paquete de fuentes.

- **Fase 2 en curso:** `contratacion` hecha (5 lecciones, 18 tarjetas, 34 preguntas). Textos oficiales descargados en `dian_2676_recursos/gestor3/` (Ley 80, 1150, 1474, 1437, 1755, 1712; D. 1082).

**Siguiente:** `procedimiento-administrativo`, `custodia-mercancias`, `ingreso-mercancias`. Falta la OPEC y confirmar la fecha del examen.
