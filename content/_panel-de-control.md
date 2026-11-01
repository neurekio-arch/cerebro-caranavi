---
tema: panel
fuentes: []
actualizado: 2026-11-01
estado: verificado
---

# 🎛️ PANEL DE CONTROL — SUBGOBERNACIÓN DE CARANAVI

> **Hoy:** `= date(today)` · 📥 Fuentes en `raw/`: **`= length(dv.pages('"raw"'))`** · 🧠 Artículos en la wiki: **`= length(dv.pages('"wiki"').where(p => p.tema))`** · 📤 Entregables: **`= length(dv.pages('"outputs"'))`**
> **Mantenido por el agente IA** (comando "panel") — requiere plugin **Dataview** activado.

---

> [!info] 🗺️ PROVINCIA DE CARANAVI — datos clave
> Creada por **D.L. 1401 (16/12/1992)**, 20.ª provincia de La Paz · **69.533 hab** (censo 2024) · ≈ **3.400 km²**
> Municipios: [[_Caranavi|Caranavi]] (59.676 hab) · [[_Alto-Beni|Alto Beni]] (Ley 4131 de 2009, capital Villa Unificada)
> ☕ **Capital Cafetalera de Bolivia** (~180 mil qq/año) · Mandarina (~213 mil qq) · Coca ~1.171 ha
> 🏛️ [[_Subgobernacion-Caranavi|Gestionada por la Subgobernación de Caranavi]] (entidad desconcentrada de la Gobernación de La Paz)

---

## 🚨 Tareas pendientes (wiki + outputs)

```dataview
TASK
FROM "wiki" OR "outputs"
WHERE !completed
LIMIT 25
```

## 🗺️ La wiki por temas

```dataview
TABLE length(rows) AS "Artículos"
FROM "wiki"
WHERE tema
GROUP BY tema
```

## 🕒 Últimos artículos actualizados

```dataview
TABLE tema AS "Tema", actualizado AS "Actualizado"
FROM "wiki"
WHERE tema
SORT file.mtime DESC
LIMIT 10
```

## 🚧 Proyectos (tema `proyectos`)

```dataview
TABLE actualizado AS "Actualizado", estado AS "Estado"
FROM "wiki/proyectos"
WHERE tema
SORT file.mtime DESC
```

## 🤖 Bitácora del agente

- 📋 [[_registro|_registro.md — qué fuentes se han compilado]]
- 📚 [[_indice-maestro|_indice-maestro.md — índice general de la wiki]]

## 🧹 Higiene (confirmar con "audita")

### Artículos huérfanos (sin enlaces)

```dataview
LIST file.name
FROM "wiki"
WHERE tema AND length(file.outlinks) = 0 AND length(file.inlinks) = 0
SORT file.name ASC
```

## 📤 Últimos entregables (outputs)

```dataview
LIST
FROM "outputs"
SORT file.mtime DESC
LIMIT 8
```

## 🔗 Accesos rápidos

| Territorio | Gestión | Visualización |
|---|---|---|
| [[territorio/_indice|🗺️ Territorio]] | [[proyectos/_indice|🚧 Proyectos]] | [[SALA_DE_SITUACION|🖼️ Sala de situación (Canvas)]] |
| [[normas/_indice|⚖️ Normas]] | [[gestion/_indice|🗂️ Gestión]] | [[Panel_Proyectos|📊 Tabla de proyectos (Bases)]] |
| [[sectores/_indice|🌾 Sectores]] | [[actores/_indice|🤝 Actores]] | Vista de grafo (Ctrl+G) filtrada por tema |
