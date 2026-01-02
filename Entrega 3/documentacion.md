# Proyecto Aurelion - Documentación

## 1. Tema
Diseñar un sistema de gestión y análisis de información centralizado para la **Tienda Aurelion**, un establecimiento ubicado en la ciudad de Bogotá, dedicado a la venta de víveres y abarrotes de la canasta familiar.

---

## 2. Problema
La tienda está presentando pérdidas económicas debido a que algunos productos tienen baja rotación y no se están vendiendo con frecuencia. Esta situación provoca acumulación de inventario, aumento de costos y disminución de las utilidades.

---

## 3. Solución
Implementar un sistema en el  **programa en Python** de gestión de inventarios y análisis de ventas que permita identificar productos de baja rotación y aplicar estrategias de promoción, optimización de compras y control de inventario.

El programa generará archivos en formato **CSV o Excel** y permitirá visualizar y analizar la información posteriormente en **Power BI**.

---

## 4. Dataset de referencia
### Fuente:
Datos de la **Tienda Aurelion**.

### Definición:
Conjunto de datos en formato Excel donde se lleva el registro correspondiente a clientes, productos y ventas.  
Se emplean cuatro tablas principales relacionadas entre sí mediante identificadores únicos.

---

## 5. Estructura 
### Tabla: clientes
| Campo             | Tipo | Escala    |
|-------------------|------|-----------|
| id_cliente        | int  | Nominal   |
| nombres_apellidos | str  | Nominal   |
| email             | str  | Nominal   |
| ciudad            | str  | Nominal   |
| fecha_registro    | date | Intervalo |

### Tabla: productos
| Campo           | Tipo | Escala  |
|-----------------|------|---------|
| id_producto     | int  | Nominal |
| nombre_producto | str  | Nominal |
| categoria       | str  | Nominal |
| precio_unitario | dec  | Razón   |

### Tabla: ventas
| Campo       | Tipo | Escala    |
|-------------|------|-----------|
| id_venta    | int  | Nominal   |
| fecha_venta | date | Intervalo |
| id_cliente  | int  | Nominal   |
| medio_pago  | str  | Nominal   |

### Tabla: detalle_ventas
| Campo           | Tipo | Escala  |
|-----------------|------|---------|
| id_venta        | int  | Nominal |
| id_producto     | int  | Nominal |
| cantidad        | int  | Razón   |
| precio_unitario | dec  | Razón   |
| importe         | dec  | Razón   |


---

## 6. Información, pasos, pseudocódigo y diagrama del programa

### 6.1 Propósito del programa

El programa en Python permitirá **consultar la documentación del proyecto de manera interactiva**, a través de un menú que se muestra en consola.  

Cada opción del menú mostrará una parte del contenido del archivo `documentacion.md`, como el tema, el problema, la solución o la estructura de la base de datos.

El usuario podrá navegar entre las opciones o salir del programa cuando lo desee.

---

### 6.2 Pasos generales del programa

1. Mostrar mensaje de bienvenida en pantalla.  
2. Mostrar el menú principal con las opciones disponibles.  
3. Leer la opción elegida por el usuario.  
4. Según la opción, mostrar el contenido correspondiente:
   - Opción 1 → Mostrar el tema  
   - Opción 2 → Mostrar el problema  
   - Opción 3 → Mostrar la solución  
   - Opción 4 → Mostrar estructura de base de datos  
   - Opción 5 → Mostrar pseudocódigo   
   - Opción 6 → Mostrar diagrama
   - Opción 7 → Salir del programa
5. Preguntar si desea volver al menú principal o finalizar.  
6. Terminar el programa al elegir “Salir”.

---

### 6.3 Pseudocódigo del programa

```text
INICIO
     MOSTRAR "Bienvenidos a la Tienda Aurelion"
    REPETIR
        MOSTRAR menú principal:
            1. Ver Tema
            2. Ver Problema
            3. Ver Solución
            4. Ver Base de Datos (lee archivos Excel)
            5. Ver Pseudocódigo y Diagrama
            6. Salir
        LEER opción seleccionada
        SEGÚN opción HACER
            CASO 1: Mostrar Tema
            CASO 2: Mostrar Problema
            CASO 3: Mostrar Solución
            CASO 4:
                Leer y mostrar datos desde archivos Excel (.xlsx)
            CASO 5: Mostrar Pseudocódigo
            CASO 6: Mostrar Diagrama
            CASO 7: Mostrar mensaje de salida y finalizar
        FIN SEGÚN
        SI opción ≠ 7 ENTONCES
            PREGUNTAR “¿Desea volver al menú principal? (1=Sí / 2=No)”
            SI respuesta = 2 ENTONCES SALIR
        FIN SI
    HASTA opción = 7 O respuesta = 2
FIN
```

---

### 6.4 Diagrama de flujo

El siguiente diagrama representa el flujo general del programa:

```mermaid
flowchart TD
    A([Inicio]) --> B[Mostrar mensaje de bienvenida]
    B --> C[Mostrar menú principal]
    C --> D[Leer opción del usuario]
    D --> E{¿Qué opción eligió?}

    E -- 1 --> F1[Mostrar Tema]
    E -- 2 --> F2[Mostrar Problema]
    E -- 3 --> F3[Mostrar Solución]
    E -- 4 --> F4[Leer y mostrar datos de archivos Excel]
    E -- 5 --> F5[Mostrar Pseudocódigo]
    E -- 6 --> F6[Mostrar Diagrama]
    E -- 7 --> G((Salir del programa))

    F1 --> H[¿Desea volver al menú principal?]
    F2 --> H
    F3 --> H
    F4 --> H
    F5 --> H
    F6 --> H

    H -- Sí --> C
    H -- No --> G

    G --> I([Fin])

---

## 7. Estadisticas Descriptivas
        cantidad    importe	       precio_unitario	ciudad_encodear	mediopago_encoder	categoria_encoder
count	 343.000000	343.000000	    343.000000	    343.000000	   343.0	            343.0
mean	 2.962099	7730.078717	    2654.495627	    2.979592	   2.460641	            1.51895
std	     1.366375	5265.543077	    1308.694720   	1.777752	   1.088508	            0.500371
min	     1.000000	272.000000	    272.000000	    1.000000	   1.0	                1.0
25%	     2.000000	3489.000000	    1618.500000	    1.000000	   1.0	                1.0
50%	     3.000000	6702.000000	    2512.000000	    3.000000	   3.0	                2.0
75%	     4.000000	10231.500000	3876.000000	    5.000000	   3.0	                2.0
max	     5.000000	24865.000000	4982.000000	    6.000000	   4.0	                2.0


## 8 Tipo de distribución de las variable
Variable Cantidad
El gráfico presentado muestra la distribución de la variable “cantidad” a través de un histograma combinado con una curva de densidad. En él se observa que los valores de cantidad se encuentran en un rango discreto entre 1 y 5, con una frecuencia relativamente equilibrada entre cada valor. El valor 2 es el más frecuente, mientras que los demás presentan conteos similares, lo que sugiere una distribución uniforme discreta. No se identifican valores atípicos ni concentraciones marcadas hacia ningún extremo, indicando que las cantidades vendidas se comportan de manera homogénea. Este tipo de gráfico es útil para comprender cómo se distribuye la variable, detectar posibles anomalías y evaluar la variabilidad en las cantidades vendidas dentro del conjunto de datos.

Variable importe
El gráfico muestra la **distribución del importe** de las ventas mediante un histograma con una curva de densidad superpuesta. Se observa que la mayoría de los valores se concentran en los importes bajos, especialmente entre 0 y 5.000, mientras que a medida que el importe aumenta, la frecuencia de registros disminuye de forma progresiva. Esta forma asimétrica indica una **distribución sesgada hacia la derecha (sesgo positivo)**, lo que significa que existen algunos valores muy altos que elevan el extremo superior de la distribución, considerados **valores atípicos o extremos**. En términos prácticos, esto sugiere que la mayoría de las transacciones tienen importes moderados, pero existen unas pocas ventas con montos considerablemente más altos. Este tipo de gráfico es útil para **analizar la dispersión de los importes**, identificar la **presencia de outliers** y comprender el **comportamiento general de las ventas** en términos de valor económico.

Variable Precio Unitario
El gráfico representa la **distribución del precio unitario** de los productos a través de un histograma con una curva de densidad superpuesta. Se observa que los precios se encuentran distribuidos en un rango amplio, entre aproximadamente 0 y 5.000, sin una forma simétrica clara. La presencia de varios picos a lo largo del eje horizontal sugiere una **distribución multimodal**, es decir, existen distintos grupos de productos con precios predominantes en diferentes intervalos. Esto puede deberse a la existencia de varias categorías de productos, como líneas económicas, intermedias y premium. No se aprecia una concentración fuerte en un único valor, aunque algunos precios altos podrían considerarse **valores atípicos**. Este tipo de gráfico sirve para **analizar la variabilidad de los precios**, identificar patrones de segmentación en los productos y detectar posibles outliers o errores de registro en los valores unitarios.

Variable ciudad
El gráfico titulado “Distribución de la ciudad” muestra la cantidad de registros asociados a cada valor codificado de la variable ciudad. Cada número en el eje horizontal representa una ciudad distinta, transformada mediante un proceso de encodeo que asigna números a categorías de texto. En el eje vertical se observa la frecuencia o número de apariciones de cada ciudad en el conjunto de datos. Se evidencia que la ciudad codificada como 1 presenta la mayor cantidad de registros, superando los 100, mientras que las demás ciudades muestran frecuencias menores y más equilibradas entre sí. Este tipo de visualización permite identificar de forma clara cuáles ciudades concentran una mayor proporción de observaciones y cuáles tienen menor representación dentro del conjunto de datos. En términos estadísticos, la distribución observada es no uniforme y sesgada, ya que la concentración de datos se encuentra marcada en ciertos valores y no sigue una forma simétrica. Este análisis resulta especialmente útil en la etapa exploratoria de los datos, ya que facilita la comprensión del comportamiento de las variables categóricas antes de aplicar modelos estadísticos o de aprendizaje automático..

Variable medio de pago
El gráfico titulado “Distribución del medio de pago” representa la frecuencia de uso de los distintos medios de pago codificados en el conjunto de datos. En el eje horizontal se muestran los valores numéricos resultantes del encodeo de la variable categórica medio de pago, mientras que en el eje vertical se observa la cantidad de registros o transacciones correspondientes a cada categoría. Se aprecia que el medio de pago codificado como 3 es el más frecuente, superando los 100 registros, mientras que los demás medios presentan frecuencias algo menores, aunque relativamente cercanas entre sí. Esto sugiere que existen preferencias más marcadas por ciertos medios de pago. Desde el punto de vista estadístico, este gráfico presenta una distribución sesgada y multimodal, ya que no hay una forma simétrica y se observan varios picos de concentración. El análisis de este tipo de distribuciones es esencial para comprender patrones de comportamiento de los clientes y posibles desequilibrios en los datos antes de aplicar modelos predictivos.

Variable categoria
El gráfico titulado “Distribución de la categoría” muestra cómo se distribuyen los registros según la variable categoría, la cual ha sido codificada numéricamente. En el eje horizontal aparecen los valores resultantes del encodeo, y en el eje vertical se refleja la cantidad de observaciones en cada categoría. Se observa que existen principalmente dos categorías (1 y 2) con una frecuencia muy similar y elevada en ambos casos, lo que indica que los datos están concentrados en estos dos grupos. La forma del gráfico evidencia una distribución bimodal, caracterizada por dos picos de frecuencia claramente definidos y una baja presencia de valores intermedios. Este tipo de distribución sugiere que el conjunto de datos agrupa los registros en dos categorías dominantes, lo cual puede ser relevante para el análisis comparativo o segmentación de clientes, productos o servicios.


## 9 Análisis de correlaciones entre variables principalees.

Matriz de Correlación
La matriz de correlación presentada muestra las relaciones lineales entre las variables numéricas del conjunto de datos. En general, los valores de correlación más cercanos a 1 o -1 indican relaciones más fuertes, mientras que los próximos a 0 reflejan asociaciones débiles o inexistentes. En este análisis, se observa que las correlaciones más destacadas se dan entre precio_unitario e importe (0.68) y entre cantidad e importe (0.60), ambas positivas y de magnitud moderadamente fuerte. Esto significa que, a medida que aumentan el precio unitario o la cantidad, también tiende a incrementarse el importe total. El resto de las variables presenta correlaciones débiles o casi nulas entre sí. Se considera que una correlación es fuerte cuando su valor absoluto supera 0.7, moderada entre 0.4 y 0.7, y débil cuando es inferior a 0.4. En conclusión, las variables precio_unitario y cantidad son las que más influyen en el importe, lo cual resulta coherente con la lógica del negocio, dado que ambas determinan directamente el valor total de una transacción


##10 Detección de outliers (valores extremos - atipicos)

Variable Cantidad
El gráfico “Distribución de cantidad” muestra la dispersión de los valores de la variable cantidad mediante un boxplot. La caja se presenta centrada y simétrica, indicando que los datos están equilibrados alrededor de la mediana. No se observan puntos fuera de los límites, por lo que no existen valores atípicos (outliers). Esto significa que todos los registros se encuentran dentro del rango normal de variación.

Dado que el conjunto total de datos es de 343 registros, el número de outliers corresponde a 0 casos, equivalentes al 0% del total. En conclusión, la variable cantidad presenta una distribución normal y sin anomalías, siendo adecuada para su análisis estadístico sin requerir ajustes adicionales.

Variable importe
El gráfico “Distribución del importe” muestra la variabilidad de los valores registrados en la variable importe mediante un boxplot. Se observa que la mayoría de los datos se concentran entre aproximadamente $3.000 y $15.000, con una mediana cercana a $8.000, lo que indica una ligera concentración de valores hacia los importes más bajos.

Sin embargo, se identifican varios valores atípicos (outliers) por encima de los $20.000, representados por los puntos fuera del rango de los bigotes. Estos casos corresponden a importes excepcionalmente altos respecto al resto de los datos. Considerando un total de 343 registros, los outliers representan un porcentaje bajo, estimado en alrededor del 2 % al 3 % del total. En conclusión, la distribución del importe presenta una tendencia sesgada hacia la derecha (cola larga positiva), debido a la presencia de valores altos aislados que incrementan la dispersión general

Variable precio unitario
La imagen muestra un diagrama de caja (boxplot) correspondiente a la variable precio_unitario. En el gráfico, no se observan puntos fuera de los bigotes del boxplot, lo que indica que no existen valores atípicos (outliers) en la distribución de esta variable.

El rango intercuartílico (IQR) representa la dispersión central de los datos, y los bigotes marcan los límites inferiores y superiores dentro del rango esperado. Dado que todos los valores se encuentran dentro de esos límites, se puede concluir que ningún registro sobrepasa los umbrales definidos por el criterio estadístico habitual (Q1 − 1.5×IQR o Q3 + 1.5×IQR).

Por tanto, la cantidad de outliers es 0, lo que implica que el porcentaje de valores atípicos respecto al total de 343 registros es del 0 %. En resumen, la variable precio_unitario presenta una distribución homogénea, sin valores extremos que puedan sesgar el análisis estadístico.

Variable Ciudad
El gráfico corresponde a un diagrama de caja (boxplot) de la variable ciudad_encodear, que representa la codificación numérica de distintas ciudades. En la visualización se aprecia que todos los valores se encuentran dentro de los límites de los bigotes, sin puntos aislados fuera de estos. Esto indica que no existen valores atípicos (outliers) en la distribución de esta variable.

El rango intercuartílico (IQR) cubre la mayor parte de los datos, y los bigotes marcan los valores mínimos y máximos dentro del rango esperado. Dado que ningún dato excede estos límites, se concluye que la variable no presenta anomalías ni valores extremos.

Por tanto, la cantidad total de outliers es 0, y considerando que el conjunto de datos cuenta con 343 registros, el porcentaje de valores atípicos es del 0 %. En resumen, la distribución de ciudad_encodear es completamente regular y no contiene desviaciones significativas que puedan afectar los análisis posteriores.

Variable Medio de pago
El diagrama de caja muestra la distribución del medio de pago codificado numéricamente (mediopago_encoder). En el gráfico no se observan puntos fuera de los bigotes, lo que indica que no existen valores atípicos en esta variable.

Por tanto, la cantidad de outliers es 0 y, considerando los 343 registros totales, el porcentaje de valores atípicos es del 0 %. En conclusión, la distribución del medio de pago es estable y no presenta valores extremos que afecten su análisis estadístico.

Variable categoria
El diagrama de caja muestra la distribución de la variable codificada categoria_encoder. En el gráfico no se observan puntos fuera de los límites o “bigotes” del boxplot, lo que indica que no existen valores atípicos en esta variable.

Por tanto, la cantidad de outliers es 0 y, considerando el total de 343 registros, el porcentaje de valores atípicos es del 0 %.

En conclusión, la distribución de la variable categoria_encoder es homogénea y no presenta valores extremos que puedan distorsionar el análisis estadístico o afectar la interpretación de los resultados.



##11 Gráficos representativos:
Estos graficos representan el aspecto clave del negocio:
* Gráfico de barras: distribución de clientes por ciudad. Muestra cuántos clientes hay en cada ciudad
La gráfica “Clientes por Ciudad” muestra la cantidad de clientes en distintas localidades.
Río Cuarto lidera con más de 100 clientes, siendo la ciudad con mayor concentración.
Le siguen Alta Gracia y Córdoba, con alrededor de 65 clientes cada una.
Carlos Paz presenta un número intermedio cercano a 45 clientes.
Mendiolaza y Villa María tienen las menores cifras, cerca de 35 clientes cada una.

* Gráfico de columnas: Medios de pago usados.
El gráfico muestra que el medio de pago más utilizado es el efectivo, seguido por QR, mientras que la transferencia y la tarjeta son los menos frecuentes. Esto indica que los usuarios prefieren métodos tradicionales y digitales en menor proporción, lo que puede orientar decisiones sobre los tipos de pago ofrecidos y estrategias comerciales

* Gráfico de Dispeción: distribución del precio unitario de los productos vs la cantidad vendida
El gráfico de dispersión muestra que la cantidad vendida varía entre uno y cinco unidades para diferentes precios unitarios, sin una correlación clara entre el precio y la cantidad. Las ventas ocurren de manera distribuida en todos los rangos de precio, lo que indica que factores distintos al precio influyen en la decisión de compra y en la cantidad vendida.

## Interpretación de los resultados orientada al problema.

La tienda está enfrentando pérdidas económicas debido a la baja rotación de algunos productos, que genera acumulación de inventario y mayores costos. El análisis de las variables revela que la cantidad vendida es bastante uniforme y sin valores atípicos, el importe de las ventas está sesgado hacia montos bajos pero con algunos valores extremos altos, y los precios unitarios presentan una distribución multimodal que apunta a diferentes segmentos de productos. Se observa que ciertas ciudades concentran mayor volumen de ventas, algunos medios de pago son claramente preferidos y las categorías de productos se agrupan principalmente en dos grandes grupos. Además, las correlaciones sugieren que el importe de las ventas depende principalmente del precio unitario y de la cantidad. La ausencia de valores atípicos en la cantidad, ciudad, medio de pago y categoría aporta estabilidad al análisis, pero los importes elevados (outliers) muestran posibles ventas excepcionales. Para abordar la problemática, se recomienda implementar estrategias de promociones en productos de baja rotación, analizar la demanda por ciudad y categoría, ajustar precios de acuerdo con los segmentos identificados y considerar acciones específicas para incentivar el uso de métodos de pago menos populares, todo esto apoyado en una gestión de inventario eficiente, análisis de datos y automatización de procesos.


##12 Objetivo Predecir
(variable a predecir)
- Predecir qué productos tendrán baja rotación en el segundo semestre de 2024 (julio a diciembre), considerando como baja rotación aquellos que registren 3 o menos compras semestrales según el comportamiento histórico de ventas.

(tipo de aprendizaje)
- Supervisado

##13 Algoritmo elegido y justificación

- Clasificación Binaria
- Elegimos la predicción de los productos que van a tener baja rotación en las proximas ventas para planificar estrategias de marketing que permitan mejorarlas.  
El aprendizaje es supervisado ya que se tienen datos de entrada y salida conocidos.
El algoritmo elegido es el de Clasificación Binaria ya que la variable a predecir es binaria (1 = baja rotación, 0 = normal/alta rotación)

##14 Entradas y salidas
(Entradas)
 #   Column                Non-Null Count  Dtype  
---  ------                --------------  -----  
 0   recencia_dias         95 non-null     int64  
 1   Rio Cuarto            95 non-null     int32  
 2   Cordoba               95 non-null     int32  
 3   Carlos Paz            95 non-null     int32  
 4   Villa Maria           95 non-null     int32  
 5   Alta Gracia           95 non-null     int32  
 6   Mendiolaza            95 non-null     int32  
 7   Alimentos             95 non-null     int32  
 8   Limpieza              95 non-null     int32  
 9   qr                    95 non-null     int32  
 10  transferencia         95 non-null     int32  
 11  efectivo              95 non-null     int32  
 12  tarjeta               95 non-null     int32  
 13  dia_semana_max_venta  95 non-null     int32  
 14  mes_max_venta         95 non-null     int32  
 15  importe_promedio      95 non-null     float64
 16  precio_promedio       95 non-null     float64

- Todas las columnas de la base de datos
(Salidas)
- 1 = baja rotación, 0 = alta rotación.

##15 Metricas de Evaluacción
- Accuracy: Porcentaje de predicciones correctas
  0.7492

##16 Modelo ML implementado
# Se importan librerías para modelos y evaluación 
# Importa el clasificador de árbol de decisión, un modelo que divide el espacio de características en reglas if/else para clasificar.
from sklearn.tree import DecisionTreeClassifier           
# Importa el clasificador Random Forest, un ensamble de múltiples árboles de decisión que votan para mejorar robustez y reducir sobreajuste          
from sklearn.ensemble import RandomForestClassifier 
 # Métricas de evaluación de modelos, como precisión y reporte de clasificación                 
from sklearn.metrics import accuracy_score, classification_report    

# Inicializar
# Se crea un árbol de decisión 
    # con semilla fija para reproducibilidad 
    # y limita la profundidad máxima a 5 niveles para controlar el sobreajuste.
# Una semilla es un número inicial que controla ese generador de números aleatorios.
# Si fijás la semilla (ejemplo: random_state=42), el algoritmo siempre va a producir los mismos resultados 
# al volver a entrenar con los mismos datos.
dt_model = DecisionTreeClassifier(random_state=42, max_depth=5) # Decision Tree 

# Crea un bosque aleatorio con semilla fija y 100 árboles, un tamaño común que equilibra rendimiento y costo computacional.
rf_model = RandomForestClassifier(random_state=42, n_estimators=100) # Random Forest

# Entrenar
# Ajusta el árbol de decisión usando las características X_train y las etiquetas Y_train.
dt_model.fit(X_train, Y_train)
# Ajusta el bosque aleatorio entrenando sus 100 árboles sobre (sub)muestras de X_train y Y_train.
rf_model.fit(X_train, Y_train)

# Predicción (se generarán predicciones sobre datos de prueba)
dt_pred = dt_model.predict(X_test)
rf_pred = rf_model.predict(X_test)

print("\n--- Resultados de Evaluación ---")

# etiquetas reales (y_true), las predicciones del modelo (y_pred) y un nombre descriptivo (name).
def evaluate_and_report(y_true, y_pred, name):
    print(f"\n### {name} ###")
    print(f"Accuracy (Precisión Global): {accuracy_score(y_true, y_pred):.4f}") # se calcula precisión con accuracy , con 4 decimales
    # Genera e imprime el reporte con métricas por clase (precision, recall, f1, soporte). 
        # target_names etiqueta las clases 0 y 1 con nombres legibles.
    # target_names[0] se asigna a la clase 0  y target_names[1] se asigna a la clase 1 por eso se pone así
    print(classification_report(y_true, y_pred, target_names=['Alta Rotación (0)', 'Baja Rotación (1)']))

evaluate_and_report(Y_test, dt_pred, "Árbol de Decisión")
evaluate_and_report(Y_test, rf_pred, "Bosque Aleatorio")

##17. División train/test entrenamiento
# Entrenar
# Ajusta el árbol de decisión usando las características X_train y las etiquetas Y_train.
dt_model.fit(X_train, Y_train)
# Ajusta el bosque aleatorio entrenando sus 100 árboles sobre (sub)muestras de X_train y Y_train.
rf_model.fit(X_train, Y_train)

##18 Predicción (se generarán predicciones sobre datos de prueba)
dt_pred = dt_model.predict(X_test)
rf_pred = rf_model.predict(X_test)


##19. Resultados en un gráfico
# Gráficoos de métricas del modelo final
# Gráfico de barras con precisión, recall y F1-score para cada clase.
import matplotlib.pyplot as plt
import numpy as np

# Datos métricas por clase
metrics = {
    "Alta rotación (0)": {"precision": 0.67, "recall": 0.67, "f1": 0.67},
    "Baja rotación (1)": {"precision": 0.70, "recall": 0.70, "f1": 0.70}
}

classes = list(metrics.keys())
precision = [metrics[c]["precision"] for c in classes]
recall = [metrics[c]["recall"] for c in classes]
f1 = [metrics[c]["f1"] for c in classes]

x = np.arange(len(classes))
width = 0.25

plt.figure(figsize=(10, 5))

plt.bar(x - width, precision, width, label="Precisión")
plt.bar(x, recall, width, label="Recall")
plt.bar(x + width, f1, width, label="F1-score")

plt.xticks(x, classes, rotation=15)
plt.ylim(0, 1.1)
plt.title("Métricas por clase")
plt.ylabel("Score")
plt.legend()
plt.grid(axis='y')

plt.show()
