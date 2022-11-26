---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.11.5
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# Modelos de clasificación para detección de fraude transaccional

Los modelos de Machine Learning utilizados para determinar si una transacción es fraudulenta o no se basan en Regresión Logística, Maquina de Soporte Vectorial y Random Forest. Estos modelos son ajustados por medio de validación cruzada estratficada toda vez que la variable de respuesta (booleana que indica si hay fraude o no), se encuentra desbalanceada toda vez que las transacciones fraudulentas tienden a una menor proporción respecto de las no fraudulentas.

En ese orden de ideas, se presentan los resultados (scoring) de los tres modelos con la validación cruzada y se exponen los resultados de la regresión logística sin validación cruzada. Por razones de capacidad de procesamiento se tomó una muestra para la construcción del modelo y validación del algoritmo.

```{Nota}
Se considera un score bueno cuando está por encima del 80%
```

## Pipelines 

Los pipelines son herramientas que se han desarrollado para optimizar el código de la maquina de aprendizaje, permiten mejorar el rendimiento del procesamiento y reducen el costo computacional.

Para más información consultar la siguiente documentación de [sklearn](https://scikit-learn.org/stable/modules/generated/sklearn.pipeline.Pipeline.html)

