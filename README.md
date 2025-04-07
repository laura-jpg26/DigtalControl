# SISTEMAS DINAMICOS MECANICOS

> Un sistema dinámico es un modelo matemático que describe cómo evolucionan las variables de un sistema a lo largo del tiempo, siguiendo ciertas reglas deterministas o probabilísticas. Estos sistemas pueden ser descritos por ecuaciones diferenciales o de diferencia y se utilizan para estudiar comportamientos como el movimiento, el crecimiento, o el cambio en diversos campos, como la física, la biología o la economía.

## 1. CONSIDERACIONES PARA DESARROLLAR UN SISTEMA DINAMICO MECANICO MASA RESOSRTE AMORTIGUADOR:

Para desarrollar un sistema dinámico mecánico que involucra una masa, un resorte y un amortiguador, como un modelo de oscilador amortiguado, hay varias consideraciones clave a tener en cuenta:

## 2 Definir el Modelo Físico:

## 2.1 Masa (m):

Es el objeto que oscila debido a la interacción con el resorte y el amortiguador. Definir su masa es crucial para calcular la inercia.

## 2.2 Resorte (k):

El resorte tiene una constante de elasticidad 𝑘 que describe su rigidez. El resorte sigue la ley de Hooke, que establece que la fuerza que ejerce el resorte es proporcional a la elongación (𝐹=−𝑘𝑥F=−kx), donde x es la deformación respecto a la posición de equilibrio.

## 2.3 Amortiguador (b):

El amortiguador se modela como una fuerza viscosa que es proporcional a la velocidad de la masa, $Famort=-b\dot{x}$ donde $\dot{x}$ es la velocidad de la masa y b es el coeficiente de amortiguamiento.

## 3. Ecuación de Movimiento:

La dinámica del sistema se puede describir mediante una ecuación diferencial de segundo orden. Para este sistema, la suma de las fuerzas es igual a la masa multiplicada por la aceleración:

$m\ddot{x}&plus;b\dot{x}&plus;kx=0$

$m\ddot{x}$ es la fuerza de inercia de la masa

$b\dot{x}$ es la fuerza de amortiguamiento

kx es la fuerza elastica de resorte 

Esta es una ecuación diferencial lineal homogénea de segundo orden.

## 4. Condiciones Iniciales:

Posición inicial x(0) y velocidad inicial $\dot{x}(0)$ son necesarias para resolver la ecuación diferencial.

Estas condiciones determinan completamente el comportamiento del sistema.

## 5. Análisis de la Solución:

Dependiendo del valor del amortiguamiento 𝑏 y la relación con la masa 𝑚 y la rigidez k, el comportamiento del sistema puede variar

## 6. Resumen

Para desarrollar un ejercicio de un sistema masa-resorte-amortiguador, debes:

Establecer el modelo físico (masa, resorte, amortiguador).

Derivar la ecuación de movimiento.

Definir las condiciones iniciales.

Analizar el tipo de amortiguamiento y encontrar la solución general.

Verificar la estabilidad y comportamiento a largo plazo.

Considerar métodos numéricos si es necesario.

Evaluar la energía y realizar una revisión física de los resultados.

Este enfoque cubre todos los aspectos esenciales para modelar y analizar el comportamiento de un sistema masa-resorte-amortiguador.

## 7. Ejercicio 1:

Una masa 𝑚=2kg cuelga de un resorte de constante 𝑘=50 N/m y está conectada a un amortiguador con coeficiente 𝑐= 5 Ns/m. El sistema oscila verticalmente bajo la acción de la gravedad.

consideraciones:

$x(0)=0.05m$ (desplazamiento desde el equilibrio)

$\dot{x}(0)=0$

![image](https://github.com/user-attachments/assets/19feb25a-b9c2-44e2-ad83-164858fbbb4e)

Diagrama de fuerzas

![image](https://github.com/user-attachments/assets/14acabfd-d7ea-46a9-a2fc-40c66c0db219)

Ecuación del movimiento

$m\ddot{x}&plus;c\dot{x}&plus;kx=0$

Aquí, la gravedad se cancela porque trabajamos respecto a la posición de equilibrio estático.

Sustituimos:

$2\ddot{x}&plus;5\dot{x}&plus;50x=0)$

$\ddot{x}&plus;2.5\dot{x}&plus;25x=0$

Cuando se considera la gravedad, la ecuación de movimiento es:

$m\ddot{x}&plus;c\dot{x}&plus;kx=mg$

Donde:x es el desplazamiento desde la posición de reposo natural (se puede definir respecto al equilibrio)

mg es la fuerza de gravedad

Podemos reorganizarla para usar en Simulink como:

$\ddot{x}=\frac{1}{m}(-c\dot{x}-kx&plus;mg)$

## Modelo en Simulink (bloques)

1. Bloques necesarios
Desde la biblioteca:

2 Integrators: para calcular velocidad y posición

Gain (3): para k, c, y 1/𝑚

Sum (2): para sumar fuerzas

Constant: para 𝑔=9.81

Product: para mg

Scope: para ver la respuesta

## Conexiones del modelo

Usa los integradores para:

$\ddot{x}\rightarrow \dot{x}\to x$

Calcula las fuerzas:

$-c\dot{x}$

$-kx&

+mg

Suma todas las fuerzas y pásalas por el bloque 1/m

El resultado es $\ddot{x}$ , lo cual alimenta el primer integrador.

Conecta x(t) al Scope.

## Parámetros del ejemplo

Masa m=2

Constante del resorte k=50

Amortiguador c=5

Gravedad g=9.81

## Grafico en simulink

![image](https://github.com/user-attachments/assets/1d5d337a-1128-4275-a6fe-2f340755c006)

## 8 Ejercicio 2:

Ejercicio: sistema de dos masas, dos resortes y un amortiguador

![image](https://github.com/user-attachments/assets/b9a9ce75-fdca-4784-9ab6-793fdef7b0bc)

Planteamiento
Dos masas están conectadas en línea sobre una superficie sin fricción:

Masa 1: 𝑚=1kg

Masa 2: m=2kg

Están conectadas con:

Resorte 1: conecta la pared a m1, constante 𝑘1=20N/m

Resorte 2: conecta 𝑚1 y m2 , constante k2 =10N/m

Amortiguador: entre m1  y m , coeficiente c=5Ns/m

Condiciones iniciales

$x_{1}(0)=0.1m,\dot{x}_{1}(0)=0$

$x_{2}(0)=0,\dot{x}_{2}(0)=0$

Ecuaciones del sistema

Para m1:

$m_{1}\ddot{x}{1}=-k{1}x_{1}-k_{2}(x_{1}-x_{2})-c(\dot{x}{1}-\dot{x}{2})$

Para m2:

$m_{2}\ddot{x}_{2}=-k_{2}(x_{2}-x_{1})-c(\hat{x}_{2}-\dot{x}_{1})$

Ahora en simulink

![image](https://github.com/user-attachments/assets/cd83871b-e83c-40a9-8760-c8a3295c8621)

## 9. Conclusiones 

Simulink permite modelar, simular y analizar sistemas dinámicos mecánicos de forma visual e intuitiva, facilitando la comprensión del comportamiento del sistema sin necesidad de resolver manualmente ecuaciones diferenciales.

## 10. Referencias 

Clase teorica
Libro Ogata, K.
