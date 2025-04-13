
## 1. MOVIMIENTO VERTICAL

En el caso vertical se debe tomar en cuenta la energía debida a la posición inicial:

$U_{0} = mgx_{0} + \frac{1}{2}k\delta^{2}$

Si está en equilibrio, entonces:

$k\delta = mg$

<p align="center">
  <img src="images/plantilla/JOAN1.png" alt="Descripción de la imagen" width="400"/>
</p>
Ahora, la energía potencial total:

$U = mg(x_{0} - x) + \frac{1}{2}k(\delta + x)^{2}$

Distribuyendo los términos:

$U = mgx_{0} - mgx + \frac{1}{2}k\delta^{2} + k\delta x + \frac{1}{2}kx^{2}$

Agrupando términos:

$U = mgx_{0} + \frac{1}{2}k\delta^{2} - (mg - k\delta)x + \frac{1}{2}kx^{2}$

Como $k\delta = mg$, entonces:

$U = U_{0} + \frac{1}{2}kx^{2}$

Energía cinética

$T = \frac{1}{2}m{x'}^{2}$

Energía total

$T + U = \frac{1}{2}m{x'}^{2} + U_{0} + \frac{1}{2}kx^{2} = \text{constante}$

Derivando para obtener la ecuación de movimiento:

$\frac{d}{dt}(T + U) = m{x'}x'' + kx{x'} = 0$

Factorizando:

$(mx'' + kx){x'} = 0$

<p align="center">
  <img src="images/plantilla/JOAN2.png" alt="Descripción de la imagen" width="400"/>
</p>

El cilindro no se desliza (conservativo)

$J = \frac{1}{2}mR^{2}$

Energía total:

$T + U = \frac{1}{2}m\dot{x}^{2} + \frac{1}{2}J\dot{\theta}^{2} + \frac{1}{2}kx^{2} = \text{constante}$

Sustituyendo $J = \frac{1}{2}mR^{2}$ y $\dot{x} = R\dot{\theta}$:

$\frac{3}{4}m\dot{x}^{2} + \frac{1}{2}kx^{2} = \text{constante}$

Derivando:

$\frac{3}{2}m\dot{x}\ddot{x} + kx\dot{x} = 0$

Factorizando:

$(m\ddot{x} + \frac{3}{2}k x)\dot{x} = 0$

Energía cinética:

$T = \frac{1}{2}m\dot{x}^{2} + \frac{1}{2}J\dot{\theta}^{2}$

Energía potencial:

$U = \frac{1}{2}kx^{2}$

Movimiento rotacional:

Usamos la relación $x = R\theta$ para expresar todo en función de $\theta$:

$\ddot{\theta} + \frac{2k}{3m}\theta = 0
Comentarios

Usualmente se utilizan para sistemas simples, ya que entre más complejo sea el sistema, más energías intervienen y más difícil se vuelve establecer el procedimiento.

## 2.SISTEMAS ELÉCTRICOS

IMAGEN
<p align="center">
  <img src="images/plantilla/JOAN3" alt="Descripción de la imagen" width="400"/>
</p>
El fenómeno físico que modela este comportamiento

El fenómeno físico que modela este comportamiento son las leyes de Kirchhoff para el circuito.

LEY DE OHM

$R = \frac{v(t)}{i(t)}$

CARGA DE UN CONDENSADOR

$i(t) = C\frac{dv(t)}{dt}$

CARGA DE UN INDUCTOR

$v(t) = L\frac{di(t)}{dt}$

EJEMPLO
<p align="center">
  <img src="images/plantilla/JOAN4" alt="Descripción de la imagen" width="400"/>
</p>

APLICANDO LEY DE KIRCHHOFF

$$
-u + v_{R} + v_{L} + v_{C} = 0
$$

$$
-u(t) + i(t) \cdot R + L\frac{di(t)}{dt} + y(t) = 0
$$

$$
i(t) = C\frac{dy(t)}{dt}
$$

*Aún no está en términos de la variable y, sustituimos i(t):*

$$
-u(t) + RC\frac{dy(t)}{dt} + LC\frac{d^{2}y(t)}{dt^{2}} + y(t) = 0
$$

## 3. Ejemplo
1.
 Obtener el modelo para el circuito de la figura:
 <p align="center">
  <img src="images/plantilla/JOAN5.png" alt="Descripción de la imagen" width="400"/>
</p>
APLICANDO LEY DE KIRCHHOFF

$$
-u + v_{R1} + v_{R2} + v_{C} = 0
$$

$$
-u + I(R_{1} + R_{2}) + v_{C} = 0
$$

$$
-u + C(R_{1} + R_{2})v_{C} + v_{C} = 0
$$

Sabemos que

$$
I_{R1} = I_{R2}
$$

Reemplazamos:

$$
\frac{u - y}{R_{1}} = \frac{y - v_{c}}{R_{2}}
$$

$$
-\frac{v_{c}}{R_{2}} = \frac{u - y}{R_{1}} = -\frac{y}{R_{2}}
$$

$$
-\frac{v_{c}}{R_{2}} = \frac{u}{R_{1}} - y \left( \frac{1}{R_{1}} + \frac{1}{R_{2}} \right)
$$

Aún no está en términos de la variable y:

$$
-v_{c} = u \frac{R_{1}}{R_{2}} - y \left( \frac{R_{2}}{R_{1}} + 1 \right)
$$

$$
v_{c} = -u \frac{R_{1}}{R_{2}} + y \left( \frac{R_{2}}{R_{1}} + 1 \right)
$$

$$
v_{c}^{'} = -u^{'} \frac{R_{1}}{R_{2}} + y^{'} \left( \frac{R_{2}}{R_{1}} + 1 \right)
$$

## 4. Ejercicios
APLICANDO LEY DE KIRCHHOFF

$$
\sum v = 0
$$

$$
-u + v_{R1} + v_{R2} + v_{R3} = 0
$$

Reemplazamos:

$$
-u(t) + i(t) \cdot R_{1} + i(t) \cdot R_{2} + i(t) \cdot R_{3} + y(t) = 0
$$

Aún no está en términos de la variable y:

$$
-u(t) + C \frac{dy(t)}{dt} \cdot R_{1} + C \frac{dy(t)}{dt} \cdot R_{2} + C \frac{dy(t)}{dt} \cdot R_{3} + y(t) = 0
$$

$$
-u(t) + C R_{1} \frac{dy(t)}{dt} + C R_{2} \frac{dy(t)}{dt} + C R_{3} \frac{dy(t)}{dt}_

<p align="center">
  <img src="images/plantilla/JOAN6.png" alt="Descripción de la imagen" width="400"/>
</p>
APLICANDO LEY DE KIRCHHOFF

$$
\sum v = 0
$$

$$
-u + v_{R1} = 0
$$

Reemplazamos:

$$
-u(t) + i(t) \cdot R_{1} + y(t) = 0
$$

Aún no está en términos de la variable y:

$$
u(t) + C \frac{dy(t)}{dt} \cdot R_{1} + y(t) = 0
$$

$$
-u(t) + C R_{1} \frac{dy(t)}{dt} + y(t) = 0
$$

---

## 4. CONCLUSIONES

Los sistemas mecánicos y eléctricos son dos grandes categorías en el estudio de los sistemas dinámicos, cada uno con sus propias características físicas, pero a menudo se pueden modelar de manera similar con matemáticas. Ambos tipos de sistemas reaccionan a estímulos externos y evolucionan con el tiempo, lo que nos permite analizarlos usando herramientas comunes como ecuaciones diferenciales, diagramas de bloques o representaciones en el espacio de estados. Por un lado, los sistemas mecánicos se basan en principios como la segunda ley de Newton y se describen en términos de desplazamiento, velocidad y fuerza. Por otro lado, los sistemas eléctricos se fundamentan en leyes como la de Ohm y las de Kirchhoff, y se describen en términos de corriente, voltaje y carga. A pesar de estas diferencias, podemos encontrar equivalencias entre ambos a través de analogías mecánico-eléctricas, lo que facilita el análisis cruzado y el diseño de soluciones interdisciplinarias. Entender tanto los sistemas mecánicos como los eléctricos dentro de la teoría de sistemas dinámicos es clave para el desarrollo de tecnologías modernas, desde el control automático de robots hasta el diseño de circuitos en la electrónica avanzada, promoviendo un enfoque integral y sistémico en la ingeniería.

---

### 5. BIBLIOGRAFÍAS

- Ogata, K. *Ingeniería de Control Moderna*. 5 edición. Prentice Hall.
- C. Chen, *Analog and Digital Control System Design*, New York, Saunders College Publishing.
- [Aulas ECCI](https://aulas.ecci.edu.co/mod/resource/view.php?id=217849)
