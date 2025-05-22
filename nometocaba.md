# DIAGRAMA  DE FLUJO DE SEÑALES
El título de cada clase, correspondiente al tema general que se trabaje en clase. Siempre después de cada título de clase, redactar una breve introducción (mínimo un párrafo) que de una mirada general al tema
## 1. DIAGRAMA DE FLUJO DE SEÑALES
>🔑 Este tipo de diagramas proporciona una forma alternativa de representar sistemas complejos, permitiendo simplificar el proceso de obtención de la función de transferencia total. Además, la fórmula de Mason resulta especialmente útil para calcular dicha función en sistemas con múltiples lazos o estructuras altamente complejas.
## 2. ELEMENTOS
*FLECHA*

<div align="center" style="display: flex; justify-content: center; gap: 20px;">

Es la relación entre las variables del sistema
  <img src="images/plantilla/flecha.png" alt="M2" width="200" height="200">
</div>

*NODO*
<div align="center" style="display: flex; justify-content: center; gap: 20px;">
  Es la representación de señales
  <img src="images/plantilla/nodo.png" alt="M2" width="200" height="200">
</div>

## 3. INTERPRETACION
Dado que el nodo representa una señal y la flecha indica la relación entre variables, cuando una flecha parte de un nodo —es decir, cuando hay una conexión de entrada a salida—, se interpreta que la señal de salida es igual a la señal de entrada multiplicada por la ganancia o relación entre esas variables.
<div align="center" style="display: flex; justify-content: center; gap: 20px;">
 
  <img src="images/plantilla/producto.png" alt="M2" width="200" height="200">
</div>

$$Y(s)=F(s)X(s)$$

Cuando varias señales convergen en un mismo nodo, se interpreta que en ese punto se realiza la suma de todas ellas, cada una multiplicada por su respectiva ganancia.
<div align="center" style="display: flex; justify-content: center; gap: 20px;">
 
  <img src="images/plantilla/sumanodos.png" alt="M2" width="200" height="200">
</div>

$$Y(s)=F_{1}(s)X_{1}(s)+F_{2}(s)X_{2}(s)-F_{3}(s)X_{3}(s)$$


## 3. DEFINICIONES

>🔑*Camino o trayectoria* : Un camino o trayectoria es un recorrido por una secuencia de ramas (aristas) conectadas siguiendo el sentido de las flechas en un grafo dirigido.

>🔑* Camino abierto* : Si en dicho recorrido no se visita ningún nodo más de una vez (es decir, no se repiten nodos), se dice que el camino o trayectoria es abierto.

>🔑*Ciclo simple* : Si el camino o trayectoria comienza y termina en el mismo nodo, y no se repite ningún otro nodo en el recorrido, se dice que es un camino o trayectoria cerrado (también conocido como ciclo simple o circuito simple).
Ganancia de lazo: Es el producto de las ganancias de las ramas que forman un lazo (ciclo).

>🔑*Trayecto o camino directo* : Es un camino que conecta un nodo de entrada con un nodo de salida, sin cruzar ningún nodo más de una vez.

>🔑*Ganancia de trayecto directo* : Es el producto de las ganancias de las ramas que componen ese trayecto directo.

>🔑*Lazo* : Un lazo es un camino o trayecto cerrado, es decir, que comienza y termina en el mismo nodo sin pasar por ningún otro nodo más de una vez.

>🔑*Ganancia de lazo* : Es el producto de las ganancias de las ramas que conforman ese lazo.



## 4. FORMULA DE MASON
$$P=\frac{1}{\Delta }\sum P_{k}\Delta _{k}$$

La fórmula de Mason, también conocida como Teorema de Mason, fue desarrollada por Samuel Jefferson Mason en la década de 1950. Es una herramienta fundamental en teoría de sistemas y control para calcular la función de transferencia de sistemas representados mediante diagramas de flujo o grafos dirigidos. La fórmula permite obtener la relación entre la salida y la entrada del sistema considerando todos los caminos directos y lazos del grafo, sin necesidad de simplificar el sistema manualmente. Esto facilita el análisis de sistemas complejos de forma sistemática y eficiente.

COEFICIENTES

- $p_k$ es la ganancia o es igual a la ganancia de los caminos directos.

- $\Delta$ es igual a $1$ menos la suma de las ganancias de los lazos, más la suma producto de los lazos que no se toquen, menos la suma producto de tres lazos que no se toquen, más puntos suspensivos.

- $\Delta_k$ es igual a $1$ menos la suma de las ganancias de los lazos que no toquen la trayectoria $P_k$, más la suma de las ganancias de los lazos que no toquen la trayectoria $P_k$ y que no se toquen entre sí, menos la suma de las ganancias de tres lazos que no toquen la trayectoria $P_k$ y que no se toquen entre sí.

###4.1💡Ejemplo 1:

<div align="center" style="display: flex; justify-content: center; gap: 20px;">
 
  <img src="images/plantilla/ejemplo1mason.png" alt="M2" width="200" height="200">
</div>

Trayectorias Directas
$P_1 = 1 \times 1 \times G_1 \times G_2 \times G_3 \times 1 = G_1 \times G_2 \times G_3$

Lazos Cerrados
$L_1 = G_1 \times G_2 \times H_1$

$L_2 = - G_2 \times G_3 \times H_2$

$L_3 = - G_1 \times G_2 \times G_3$

$\Delta = 1 - L_1 + L_2 + L_3$

$\Delta_1 = 1$, porque todos los lazos tocan a $P_k$
$\frac{C(s)}{R(s)} = \frac{P_1 \times \Delta_1}{\Delta} = \frac{G_1 \times G_2 \times G_3}{1 - G_1 \times G_2 \times H_1 + G_2 \times G_3 \times H_2 + G_1 \times G_2 \times G_3}$



## 5. Ecuaciones
Para la edición de ecuaciones debe utilizar la etiqueta '$$' al comienzo y final de la ecuación para que la ecuación quede centrada ocupando una línea. Si se quiere que la ecuación quede integrada en el texto debe utilizar la etiqueta '$' al comienzo y final de la ecuación. Las ecuaciones pueden ser editadas utilizando el código LATEX, en el siguiente enlace encuentran un editor de ecuaciones que les genera el código. http://www.alciro.org/tools/matematicas/editor-ecuaciones.jsp . Sin embargo hay muchas otras herramientas que pueden utilizar para esto.

💡**Ejemplo 1:** si se va a representar la ecuación de la ley de Ohm se puede mostrar así $R=\frac{V}{I}$ o también,

$$R=\frac{V}{I}$$

$${
\begin{pmatrix*}[r]
63 & 71 & 2\\
6 & 829 & 12\\
599 & 9 & 361
\end{pmatrix*}
}={\begin{pmatrix*}[r]
63 & 71 & 2\\
6 & 829 & 12\\
599 & 9 & 361
\end{pmatrix*}}$$


## 6. Figuras
Todas las figuras que incluya deben ser generadas por ustedes, **no utilizar las figuras de las presentaciones**. Para incluir figuras puede seguir los siguientes pasos:
* Primero escribimos ![]().
* Después escribimos, dentro de los corchetes, el texto alternativo. Este es opcional y solo entra en acción cuando no se puede cargar la imagen correctamente.
* Después escribimos, dentro de los paréntesis, la ubicación del archivo (ya sea una url o una ubicación dentro de algun folder local). Se recomienda poner las imágenes en una carpeta que se llame imágenes dentro del repositorio github para que no tengan problemas al cargar las imágenes.

💡**Ejemplo 2:**

![Figura de prueba](images/plantilla/Captura2.PNG)

Figura 1. Figura de prueba

Incluya la respectiva etiqueta a modo de descripción de la figura y mantenga numeración consecutiva para todas las figuras de la clase.

## 7. Tablas
En caso de necesitar la inclusión de tablas para organizar información se recomienda el uso de la herramienta del siguiente enlace https://www.tablesgenerator.com/markdown_tables , la cual permite organizar la información dentro de la tabla y genera el código markdown automáticamente:

💡**Ejemplo 3:** 

| **Resultado** | **x = número de intentos hasta primer éxito** |
|---------------|-----------------------------------------------|
|       S       |                       1                       |
|       FS      |                       2                       |
|      FFS      |                       3                       |
|      ...      |                      ...                      |
|    FFFFFFS    |                       7                       |
|      ...      |                      ...                      |

Tabla 1. Tabla de ejemplo

Cada tabla debe llevar la etiqueta que describa su contenido y numeración consecutiva para todas las tablas

## 8. Código
Teniendo en cuenta que el curso requiere del desarrollo de código matlab, c, c++ u otro. Si requiere incluir pequeños segmentos de código en los apuntes hágalos de la siguiente manera:

💡**Ejemplo 4:**
```
var sumar2 = function(numero) {
  return numero + 2;
}
```

## 9. Ejercicios
Deben agregar 2 ejercicios con su respectiva solución, referentes a los temas tratados en cada una de las clases. Para agregar estos, utilice la etiqueta #, es decir como un nuevo título dentro de la clase con la palabra 'Ejercicios'. Cada uno de los ejercicios debe estar numerado y con su respectiva solución inmediatamente despues del enunciado. Antes del subtitulo de cada ejercicio incluya el emoji 📚

## Rúbrica
| 0-1                                                                                   | 1-2                                                                                  | 2-3                                                                                                                                                                               | 3-4                                                                                                                                                                       | 4-5                                                                                                                                                                               |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Presenta menos del 10% de los temas o no presenta por  el medio y formato  solicitado | Presenta menos del 40% de los temas solicitados, y  cumple parcialmente la plantilla | Presenta menos del 60% de los temas solicitados (con descripciones, gráficos tablas, etc), y cumple  parcialmente la plantilla. No presenta la totalidad  de ejercicios resueltos | Presenta menos del 80% de los temas solicitados (con descripciones, gráficos, tablas, etc) y cumple con  la plantilla. No presenta  la totalidad de ejercicios  resueltos | Presenta el 100% de los temas vistos en clase (con descripciones, gráficos, tablas, etc), siguiendo totalmente la plantilla. presenta la  totalidad de los ejercicios solicitados |

## 10. Conclusiones
Agregue unas breves conclusiones sobre los temas trabajados en cada clase, puede ser a modo de resumen de lo trabajado o a indicando lo aprendido en cada clase

## 11. Referencias
Agregue un subtítulo al final donde pueda poner todas las referencias consultadas incluyendo el origen o fuente de los ejercicios planteados. Tambien dentro del texto referencie los textos o artículos consultados y las figuras y tablas dentro de la explicación de las mismas.





