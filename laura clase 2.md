
# ÁLGEBRA DE BLOQUES

Durante esta clase se abordó el concepto de **álgebra de bloques**, una herramienta visual y matemática que permite representar y simplificar sistemas dinámicos. Este método fue introducido por **J. Watts**, quien desarrolló una serie de diagramas para representar el funcionamiento de la **máquina de vapor** y entender cómo fluían las señales dentro del sistema.

## 1. Elementos del álgebra de bloques

### 🔹 Bloque funcional

Representa una **operación matemática** o el conjunto de **reglas** que transforman una señal. Generalmente, contiene funciones como ganancias, derivadas, integrales o funciones de transferencia.

<div align="center" style="display: flex; justify-content: center; gap: 20px;">

  <img src="images/plantilla/bloque_funcional.png" width="450" height="250">

</div>

---

### 🔹 Flechas (Señales)

Representan el **flujo de información** dentro del sistema. Cada flecha simboliza una **señal** o una **variable** que se transmite de un bloque a otro.

<div align="center" style="display: flex; justify-content: center; gap: 20px;">

  <img src="images/plantilla/flechas_senales.png" width="450" height="250">

</div>

---

### 🔹 Punto de suma

Indica la realización de una **operación algebraica** entre señales (suma o resta), siempre que sean **de las mismas dimensiones**.

<div align="center" style="display: flex; justify-content: center; gap: 20px;">

  <img src="images/plantilla/punto_suma.png" width="450" height="250">

</div>

---

### 🔹 Ramificación

Se usa para representar una **derivación** de la misma señal hacia varios bloques. Esto permite que una única variable sea utilizada en distintos procesos simultáneamente.

<div align="center" style="display: flex; justify-content: center; gap: 20px;">

  <img src="images/plantilla/ramificacion.png" width="450" height="250">

</div>

---

## 2. Interpretación del diagrama

<div align="center" style="display: flex; justify-content: center; gap: 20px;">

  <img src="images/plantilla/interpretacion_basica.png" width="500" height="300">

</div>

### 🔑 Cuando se tiene un sistema con una **entrada**, una **función de transferencia** y una **salida**, se interpreta matemáticamente como:

$Y(s) = G(s) \cdot U(s)$

---

## 3. Composición de sistemas (dos bloques en serie)

Cuando hay **dos sistemas conectados en cascada**, se puede realizar una deducción matemática paso a paso. Supongamos dos funciones de transferencia conectadas en serie, **G₁(s)** y **G₂(s)**:

<div align="center" style="display: flex; justify-content: center; gap: 20px;">

  <img src="images/plantilla/dos_bloques_serie.png" width="500" height="300">

</div>

Entonces, se describe el comportamiento del sistema así:

* $\frac{Y_1(s)}{U_1(s)} = G_1(s)$
* $\frac{Y_2(s)}{U_2(s)} = G_2(s)$

Si además sabemos que:

* $U_2(s) = Y_1(s)$

Entonces:

### 📌 Paso 1:

$Y_1(s) = U_1(s) \cdot G_1(s)$

### 📌 Paso 2:

$Y_2(s) = Y_1(s) \cdot G_2(s)$

### 📌 Paso 3:

$Y_2(s) = U_1(s) \cdot G_1(s) \cdot G_2(s)$

### 📌 Resultado final:

$\frac{Y_2(s)}{U_1(s)} = G_1(s) \cdot G_2(s)$

---

¿Quieres que continúe con más ejemplos o con combinaciones distintas como lazos de retroalimentación o sistemas en paralelo?

