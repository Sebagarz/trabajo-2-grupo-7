# Bienestar subjetivo en personas mayores chilenas

Reporte abierto desarrollado para el curso de Ciencia Social Abierta,
Departamento de Sociología, Universidad de Chile.

Este repositorio implementa, como Quarto Book reproducible, los 8 puntos de
la pauta de "Reporte abierto":

| # | Punto de la pauta | Dónde está en este repositorio |
|---|---|---|
| 1 | Introducción (resumen) | `index.qmd` (abstract) y `01-introduccion.qmd` |
| 2 | Tema y motivación | `01-introduccion.qmd`, `02-antecedentes.qmd` |
| 3 | Hipótesis preregistradas | `03-hipotesis.qmd` + `input/prereg/preregistro.md` |
| 4 | Datos abiertos | `04-metodos.qmd` (sección "Datos abiertos") |
| 5 | Protocolo IPO | `04-metodos.qmd` (sección "Protocolo de investigación") |
| 6 | Registro en OSF | Pendiente: ver instrucciones más abajo |
| 7 | Preprint | Pendiente: ver instrucciones más abajo |
| 8 | Quarto Book reproducible en repo público | Este repositorio |

## Requisitos previos

- Quarto 1.5 o superior (<https://quarto.org>).
- Motor LaTeX para la salida PDF (TinyTeX, TeX Live o MiKTeX).
- R con los paquetes listados en `procesamiento/preparacion.qmd` y
  `procesamiento/analisis.qmd` si se quiere reejecutar el análisis.
- Git para clonar y versionar.

## Cómo reproducir el análisis

1. Descargar la base original de la EBS 2023 desde el sitio del
   Observatorio Social (ver `input/README.md`) y guardarla en
   `input/data-orig/EBS_2023.RData`.
2. Renderizar `procesamiento/preparacion.qmd` para generar la base limpia
   en `input/data-proc/`.
3. Renderizar `procesamiento/analisis.qmd` para generar las tablas en
   `output/tables/`.
4. Renderizar el libro completo:
   ```
   quarto render --to html pdf
   ```
5. El sitio se publica desde `docs/` (configurado en `_quarto.yml`).

## Pendientes para completar la entrega (pasos manuales)

Estos tres pasos no pueden completarse desde el repositorio mismo; quedan
documentados aquí como checklist:

- [ ] **Crear cuenta y proyecto en OSF** (osf.io): subir
  `input/prereg/preregistro.md`, este `README.md` y, opcionalmente, el PDF
  del manuscrito una vez generado. Pegar el enlace del proyecto OSF en
  `03-hipotesis.qmd` y en `input/prereg/preregistro.md`.
- [ ] **Crear repositorio público en GitHub**, subir este contenido, y
  activar GitHub Pages apuntando a la carpeta `docs/`. Actualizar la
  `repo-url` en `_quarto.yml` con la URL real.
- [ ] **Generar y publicar el preprint**: el PDF que produce
  `quarto render --to pdf` puede subirse directamente a un servidor de
  preprints (p. ej. SciELO Preprints, OSF Preprints) o dejarse disponible
  como release del repositorio de GitHub. Agregar el enlace en
  `input/prereg/preregistro.md`.

## Estructura del repositorio

- `index.qmd`, `01`–`06-*.qmd`: capítulos del libro.
- `apendices/`: anexos (instrumentos, tablas adicionales).
- `input/`: datos crudos (`data-orig/`), datos procesados (`data-proc/`),
  preregistro (`prereg/`) y bibliografía adicional (`bib/`).
- `output/`: tablas y gráficos generados por el análisis.
- `procesamiento/`: scripts reproducibles (`preparacion.qmd`,
  `analisis.qmd`).
- `refs/`: bibliografía (`referencias.bib`) y estilo de citación
  (`apa.csl`).
- `assets/`, `includes/`: identidad visual y configuración de portada/PDF
  (no requieren edición para este trabajo).
