# Clasificación de sentimiento en reseñas de usuarios

Proyecto de la asignatura **Modelos Secuenciales**
---

## Objetivo

Construir un modelo secuencial capaz de determinar la **polaridad de una reseña escrita por un
usuario** —negativa, neutral o positiva— a partir únicamente de su texto, sin recurrir a la
calificación numérica que el usuario asignó al producto.

El interés del problema está en que el sentimiento no vive en las palabras aisladas sino en el
**orden en que aparecen**: expresiones como *"no está mal"* o *"esperaba más"* solo se interpretan
correctamente leyendo la frase completa. Por esa razón el proyecto se aborda con arquitecturas
secuenciales, capaces de retener contexto a lo largo de la lectura, y no con modelos que traten el
texto como un simple conteo de términos.

## Alcance

El proyecto sigue el ciclo de vida completo de un desarrollo de ciencia de datos y avanza por
unidades:

| Unidad | Etapa | Estado |
| :---: | :--- | :--- |
| 1 | Selección del dataset y pipeline de preprocesamiento | Completada |
| 2+ | Diseño, entrenamiento y evaluación de los modelos secuenciales | Aun no se ha iniciado|

Actualmente el repositorio contiene el resultado de la primera etapa: un conjunto de datos
depurado, trazable y transformado en secuencias numéricas de longitud fija, listo para alimentar
los modelos de las unidades siguientes.

## Datos

**Amazon Fine Food Reviews** (McAuley y Leskovec, 2013): 568.454 reseñas de productos alimenticios
publicadas entre 1999 y 2012. Se eligió por su volumen, por incluir marca temporal —lo que permite
evaluar el modelo prediciendo hacia adelante, como ocurriría en un escenario real— y porque la
etiqueta puede derivarse de la calificación sin anotación manual.

## Contenido del repositorio

- `notebooks/` — notebook ejecutable del pipeline de preprocesamiento.
- `docs/` — reporte técnico con las decisiones, los resultados y las limitaciones.
- `artifacts/` — vocabulario y parámetros del pipeline.

## Referencia del conjunto de datos

McAuley, J., y Leskovec, J. (2013). *Amazon Fine Food Reviews* [Conjunto de datos]. Kaggle.
https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews

---
