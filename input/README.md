# Carpeta `input`

Insumos externos del proyecto "Bienestar subjetivo en personas mayores
chilenas".

- `data-orig/`: base original de la Encuesta de Bienestar Social (EBS)
  2023. **No se incluye en el repositorio por su tamaño**; debe
  descargarse desde el sitio del Observatorio Social del Ministerio de
  Desarrollo Social y Familia:
  <https://observatorio.ministeriodesarrollosocial.gob.cl/encuesta-bienestar-social-2023>
  y guardarse como `input/data-orig/EBS_2023.RData`.
- `data-proc/`: base procesada (`base_ebs_limpia.Rdata`), generada por
  `procesamiento/preparacion.qmd`. Tampoco se versiona en GitHub si supera
  el límite recomendado de tamaño; se puede regenerar ejecutando el script.
- `prereg/`: copia del preregistro depositado en OSF (ver enlace en
  `03-hipotesis.qmd`).
- `bib/`: bibliografías adicionales en formato `.bib`/`.ris`, si las hubiera.

> Los microdatos de la EBS 2023 son de acceso público; no requieren
> solicitud de permiso, solo descarga directa desde el sitio del Ministerio.

