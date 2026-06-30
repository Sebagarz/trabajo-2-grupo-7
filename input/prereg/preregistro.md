# Preregistro: Bienestar subjetivo en personas mayores chilenas

**Proyecto:** Bienestar subjetivo en personas mayores chilenas: una
aproximación sociológica desde condiciones estructurales y experiencias de
vida.

**Equipo:** Catalina Parra A., Eduardo Ortiz A., Juan Gutiérrez García— Departamento de
Sociología, Universidad de Chile.

**Curso:** Ciencia Social Abierta, Juan Castillo V., 30/06/2026.

**Fecha de este registro:** 30/06/2026

---

## 1. Nota de transparencia metodológica

Este preregistro formaliza, bajo prácticas de ciencia abierta, un análisis cuyas hipótesis fueron especificadas a priori en el marco de un trabajo del curso de Estadística Multivariada, y cuyos modelos de regresión ya habían sido estimados antes de la creación de este registro. **No se trata, por lo tanto, de un preregistro confirmatorio en sentido estricto** —en el cual las hipótesis se fijan y se hacen públicas antes de cualquier contacto con los
datos. Se declara esta condición de forma explícita, antes de presentar el resto del protocolo, por compromiso con la transparencia del proceso de investigación.

## 2. Pregunta de investigación

¿En qué medida las condiciones económicas, de salud y relacionales se
asocian con el bienestar subjetivo de las personas mayores chilenas
(60 a 79 años)?

## 3. Hipótesis

Modelo general:
IBS = β0 + β1·ss6 + β2·yy2 + β3·yy3 + β4·ss1 + β5·rr1 + ε

- **H1.** Mayor protección financiera en salud (ss6) → mayor IBS (efecto
  positivo).
- **H2.** Mayor capacidad del hogar para llegar a fin de mes (yy2) → mayor
  IBS (efecto positivo).
- **H3.** Mayor ingreso subjetivo necesario (yy3) → menor IBS (efecto
  negativo).
- **H4.** Mejor estado de salud autopercibido (ss1) → mayor IBS (efecto
  positivo).
- **H5.** Mayor tamaño de la red de apoyo social (rr1) → mayor IBS (efecto
  positivo).

## 4. Datos

- **Fuente:** Encuesta de Bienestar Social (EBS) 2023, Ministerio de
  Desarrollo Social y Familia de Chile.
- **Acceso:** datos públicos, descarga directa desde
  <https://observatorio.ministeriodesarrollosocial.gob.cl/encuesta-bienestar-social-2023>
- **Población de estudio:** personas de 60 a 79 años residentes en
  viviendas particulares en Chile (submuestra de la EBS 2023, N original =
  11.234; N tras filtro de edad = 3.170; N tras casos completos = 2.994).

## 5. Variables

| Variable | Tipo | Construcción |
|---|---|---|
| IBS (dependiente) | Intervalar (promedio Likert 1-5) | Promedio de a1, a2_a, a2_b, a12 |
| ss6 | Dummy (0/1) | Recodificación de ítem ordinal 1-5 |
| yy2 | Dummy (0/1) | Recodificación de ítem ordinal 1-5 |
| yy3 | Razón (millones de pesos) | Ítem original reescalado |
| ss1 | Dummy (0/1) | Recodificación de ítem ordinal 1-5 |
| rr1 | Razón (conteo 0-130) | Ítem original |

## 6. Plan de análisis preespecificado

1. Estadística descriptiva univariada de IBS y predictores.
2. Correlaciones de Pearson bivariadas entre cada predictor y el IBS.
3. Regresión lineal jerárquica en tres etapas: (a) dimensión económica,
   (b) + dimensión salud, (c) + dimensión relacional.
4. Cálculo de coeficientes estandarizados sobre el modelo completo.

## 7. Criterios de exclusión

Se excluyen personas de 80 años o más (riesgo de sesgo en autorreporte por
deterioro cognitivo) y casos con valores perdidos en cualquiera de las
variables del modelo (listwise deletion; pérdida esperada < 5%).

## 8. Materiales asociados

- Protocolo completo (estructura IPO): ver `04-metodos.qmd` en el
  repositorio del proyecto.
- Scripts reproducibles: `procesamiento/preparacion.qmd` y
  `procesamiento/analisis.qmd`.
- Repositorio público: [COMPLETAR URL DE GITHUB]
- Preprint: [COMPLETAR URL DEL PREPRINT]
