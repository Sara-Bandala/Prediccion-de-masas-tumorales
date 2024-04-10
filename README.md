# Proyecto de predicción de masa tumoral en mamografías 
## Elaboro: Sara Bandala

La mamografía es el método más eficaz para la detección del cáncer de mama disponible. Sin embargo, las prediciones de valores positivos de una biopsia resultante de la interpretación de la mamografía conduce a aproximadamente 70% biopsias innecesarias con resultados benignos.

Es innecesario el estrés y la cirugía que se deriva de los falsos positivos obtenidos de los resultados de la mamografía. Si podemos construir una mejor manera de interpretarlos a traves del Machine Learning, se podría mejorar la calidad de vida de muchas personas.

### Objetivo: 
Predecir si una masa tumoral en una mamografía es benigna o maligna. Se hizo uso del conjunto de datos públicos de "masas mamográficas" del repositorio de UCI. Disponible [aqui](https://archive.ics.uci.edu/dataset/161/mammographic+mass). Esta base contiene 961 casos de masas tumorales detectadas en mamografías. El archivo contiene los siguientes atributos:

* Evaluación BI-RADS: 1 a 5 (ordinal).
* Edad: edad del paciente en años (entero)
* Forma:forma de la masa:redonda=1 ovalada=2 lobular=3 irregular=4 (nominal)
* Margen:margen de masa: circunscrito=1 microlobulado=2 oscurecido=3 mal definido=4 espiculado=5 (nominal).
* Densidad:densidad de masa alta = 1 iso = 2 baja = 3 que contiene grasa = 4 (ordinal)
* Gravedad:benigno=0 o maligno=1 (binomial)(Target)

BI-RADS es una evaluación de cuán confiable es la clasificación de gravedad; no es un atributo "predictivo" por lo que se descarta. Los atributos de edad, forma, margen y densidad son las características con las que construiremos nuestro modelo, y "gravedad" es la clasificación que intentaremos predecir en función de esos atributos. Aunque "forma" y "margen" son tipos de datos nominales, que sklearn normalmente no trata bien, están lo suficientemente cerca de los ordinales como para que no debamos descartarlos. La "forma", por ejemplo, se ordena cada vez más de redonda a irregular.

### Modelos empleados 
* Regresión Logística 
* SVM
* SVM con kernel
* Decision trees 
* Random Forest
* XGBoost
* KNN ponderados
* Naive Bayes
* Red Neuronal
* Red Neuronal con validacion cruzada

Se logro una exactitud del 89.9%
