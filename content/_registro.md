---
tema: registro
fuentes: []
actualizado: 2026-11-01
estado: verificado
---

# 📋 REGISTRO DE COMPILACIONES (append-only)

> **Bitácora del agente** — método del video: nunca se editan ni borran entradas viejas.
> Formato: `## [AAAA-MM-DD] compila — archivos de raw/ procesados → artículos creados/modificados + dudas`

---

## [2026-10-31] instalación — Kit del método del video (Karpathy) + Panel de Control
- Creados `wiki/_indice-maestro.md`, `wiki/_registro.md`, `wiki/_panel-de-control.md`, `extras/` (SALA_DE_SITUACION.canvas, Panel_Proyectos.base).

## [2026-10-31] compila — raw/02_Territorio/Ley-4131-Alto-Beni
- Procesada la transcripción de la Ley 4131 (Lexivox BO-L-4131).
- Creados: `wiki/normas/_Ley-4131.md` · `wiki/territorio/_Alto-Beni.md` · `wiki/territorio/_Provincia-Caranavi.md` · índices de ambos temas.
- Dudas/huecos: censo INE 2024 por municipio y comunidad; lista oficial de distritos municipales; PDF oficial de la Gaceta; pendientes `_DL-1401` y `_Ley-031`; artículo `_Caranavi`.

## [2026-10-31] compila — semillas del plan + fuentes reales de la Subgobernación
- Procesados 5 recortes: Wikipedia (Provincia, Municipio), caranavi.gob.bo, Avenida Cívica Bs 15M, noticias de la Subgobernación.
- Creados: `_DL-1401`, `_Caranavi`, `_Subgobernacion-Caranavi`, `_GAM-Caranavi`, `_Avenida-Civica` + índices de actores y proyectos.
- Actualizados: `_Provincia-Caranavi` (verificado), índices de territorio y normas.
- Dudas/huecos: texto del D.L. 1401 (no está en Lexivox → Gaceta); fecha de posesión de la subgobernadora Eva Marleny Colque; lista nominal de los 5 distritos de Caranavi y distritos de Alto Beni; detalle técnico de la Avenida Cívica; organigrama y POA de la Subgobernación; GAM Alto Beni.

## [2026-11-01] compila — PRUEBA del flujo raw → compila (documento demo)
- Procesado `raw/04_Gestion/2026-11-01_demo-oficio-TEST.md` (oficio DEMO, no real).
- Creados: `wiki/gestion/_Oficio-demo-AG123.md` · `wiki/gestion/_indice.md`.
- Objetivo: demostrar el ciclo completo `raw → compila → wiki → índices → registro`.
- ⚠️ Ambos archivos marcados como PRUEBA — eliminar tras la práctica.

## [2026-11-01] LINTER — incidente de sincronización y regeneración
- El sync cruzado entre bóvedas eliminó los artículos de `wiki/` (propagación de borrados desde una bóveda parcial del celular).
- El agente REGENERÓ los 16 archivos de `wiki/` desde su fuente de conocimiento. Sin pérdida de información.
- Regla reforzada: una sola bóveda por dispositivo; nunca sincronizar bóvedas parciales.
