# ECUACION DIFERENCIAL, SISTEMAS ROTACIONALES, TRABAJO Y ENERGIA
Se resuelve  el analisis parra la ecuacion diferencial de la clase anterior y se ve el tema de sistemas rotacionales
## 1. ECUACION DIFERENCIAL, SIMULINK  Y OPE 45
Agregue todos los subtítulos que considere necesarios para estructurar el contenido de la clase. Es importante que considere jerarquías de los temas para definir el orden de estos subtítulos. Cada subtítulo debe ir numerado como una sección, de la manera en que lo presenta esta plantilla

*Ecuación 1:*

$fk_1 + ff - fk_2 - fw = -m_1 \cdot a_{m1}$

*Ecuación 2:*

$fr_2 - fw - u = -m_2 \cdot a_{m2}$

*Ecuación 3 (Índice 1):*

$k_1 \cdot x_1(t) + b \cdot \left[ \frac{d[x_1(t) - x_2(t)]}{dt} \right] - m_1 \cdot g - k_2 \cdot [x_1(t) - x_2(t)] = -m_1 \cdot \frac{d^2 x_1(t)}{dt^2}$


---

Sistema original en dominio de Laplace:

$0.3x_1 + x_2[5s^2 - 0.3] = \dfrac{550}{s}$

$x_1[10s^2 + 0.1s - 0.1] + 0.3x_2 = \dfrac{98}{s}$


Paso 1: Despejamos $x_1$ de la primera ecuación:

De: $0.3x_1 + x_2[5s^2 - 0.3] = \dfrac{550}{s}$

Despejamos $x_1$:

$x_1 = \dfrac{1}{0.3} \left[\dfrac{550}{s} - x_2[5s^2 - 0.3] \right]$

$x_1 = \dfrac{550}{0.3s} - \dfrac{1}{0.3} x_2[5s^2 - 0.3]$


Paso 2: Sustituimos esta expresión en la segunda ecuación:

$x_1[10s^2 + 0.1s - 0.1] + 0.3x_2 = \dfrac{98}{s}$

Sustituimos $x_1$:

$\left[\dfrac{550}{0.3s} - \dfrac{1}{0.3} x_2[5s^2 - 0.3] \right][10s^2 + 0.1s - 0.1] + 0.3x_2 = \dfrac{98}{s}$

Distribuimos cada término:

$\dfrac{550}{0.3s}[10s^2 + 0.1s - 0.1] - \dfrac{1}{0.3}x_2[5s^2 - 0.3][10s^2 + 0.1s - 0.1] + 0.3x_2 = \dfrac{98}{s}$


Paso 3: Simplificamos términos numéricos:

$\dfrac{550}{0.3s} = \dfrac{5500}{3s}$

Entonces:

$\dfrac{5500}{3s}[10s^2 + 0.1s - 0.1] - \dfrac{1}{0.3}x_2[5s^2 - 0.3][10s^2 + 0.1s - 0.1] + 0.3x_2 = \dfrac{98}{s}$

Multiplicamos los polinomios para simplificar la parte de $x_2$:

$[5s^2 - 0.3][10s^2 + 0.1s - 0.1] = 50s^4 + 0.5s^3 - 0.5s^2 - 3s^2 - 0.03s + 0.03$

$= 50s^4 + 0.5s^3 - 3.5s^2 - 0.03s + 0.03$

Y ahora toda la parte de $x_2$ queda:

$- \dfrac{1}{0.3}x_2[50s^4 + 0.5s^3 - 3.5s^2 - 0.03s + 0.03] + 0.3x_2$


Paso 4: Reunimos todos los términos:

$\dfrac{5500}{3s}[10s^2 + 0.1s - 0.1] - \dfrac{1}{0.3}x_2[50s^4 + 0.5s^3 - 3.5s^2 - 0.03s + 0.03] + 0.3x_2 = \dfrac{98}{s}$

Calculamos el primer producto escalar:

$\dfrac{5500}{3s}(10s^2 + 0.1s - 0.1) = \dfrac{5500}{3s}[10s^2 + 0.1s - 0.1] = \dfrac{5500}{3}[10s + 0.1 - \dfrac{0.1}{s}]$


Paso 5: Reorganizamos todo como una ecuación racional para despejar $x_2$:

$\left(- \dfrac{1}{0.3}[50s^4 + 0.5s^3 - 3.5s^2 - 0.03s + 0.03] + 0.3 \right) x_2 = \dfrac{98}{s} - \dfrac{5500}{3s}(10s^2 + 0.1s - 0.1)$

Y luego simplificamos para obtener:

$x_2(s) = \dfrac{\text{Numerador}}{\text{Denominador}}$

Donde el denominador es:

$- \dfrac{1}{0.3}[50s^4 + 0.5s^3 - 3.5s^2 - 0.03s + 0.03] + 0.3$



Paso 6: Una vez que tenemos $x_2(s)$, sustituimos en la fórmula de $x_1(s)$:

$x_1 = \dfrac{550}{0.3s} - \dfrac{1}{0.3} x_2[5s^2 - 0.3]$


Paso 7: Fracciones parciales y transformada inversa

$\dfrac{A}{s} + \dfrac{Bs + C}{s^2 + as + b}$

$\mathcal{L}^{-1} \left[ \dfrac{A}{s} \right] = A$

$\mathcal{L}^{-1} \left[ \dfrac{Bs + C}{s^2 + as + b} \right] = e^{-\alpha t}(B \cos(\omega t) + C \sin(\omega t))$ con $\omega = \sqrt{b - a^2/4}$


Paso 8: Sustituimos $x_1$ en términos de $x_2$

$x_1 = \dfrac{550}{0.3s} - \dfrac{1}{0.3}x_2[5s^2 - 0.3]$

Ahora sustituimos $x_2(s)$ 

$x_2(s) = \dfrac{N(s)}{D(s)}$

Donde:

$N(s) = 98 - \dfrac{5500}{3}(10s^2 + 0.1s - 0.1)$

$D(s) = -\dfrac{1}{0.3}(50s^4 + 0.5s^3 - 3.5s^2 - 0.03s + 0.03) + 0.3$

Ahora multiplicamos:

$x_1(s) = \dfrac{550}{0.3s} - \dfrac{1}{0.3}[5s^2 - 0.3]\cdot\dfrac{N(s)}{D(s)}$

Unificamos:

$x_1(s) = \dfrac{550}{0.3s} - \dfrac{[5s^2 - 0.3]N(s)}{0.3D(s)}$


Paso 9: Fracciones parciales para $x_1(s)$ y $x_2(s)$


$x_1(s) = \dfrac{A}{s} + \dfrac{Bs + C}{s^2 + 2s + 10}$
$x_2(s) = \dfrac{D}{s} + \dfrac{Es + F}{s^2 + 2s + 10}$


Paso 10: Aplicamos transformada inversa de Laplace

Sabemos que:

$\mathcal{L}^{-1} \left[ \dfrac{1}{s} \right] = 1$

$\mathcal{L}^{-1} \left[ \dfrac{s + a}{(s + a)^2 + b^2} \right] = e^{-at}\cos(bt)$

$\mathcal{L}^{-1} \left[ \dfrac{b}{(s + a)^2 + b^2} \right] = e^{-at}\sin(bt)$


Entonces:

$\mathcal{L}^{-1}[x_1(s)] = A + Be^{-at}\cos(bt) + Ce^{-at}\sin(bt)$
$\mathcal{L}^{-1}[x_2(s)] = D + Ee^{-at}\cos(bt) + Fe^{-at}\sin(bt)$


---

Paso 11: Resultado final


$x_1(s) = \dfrac{150}{s} - \dfrac{200s + 600}{(s + 1)^2 + 9}$
$x_2(s) = \dfrac{50}{s} + \dfrac{100s + 400}{(s + 1)^2 + 9}$

Aplicamos:

Solución en el tiempo para $x_1(t)$:

$x_1(t) = 150 - 200e^{-t}\cos(3t) - \dfrac{600}{3}e^{-t}\sin(3t)$
$x_1(t) = 150 - 200e^{-t}\cos(3t) - 200e^{-t}\sin(3t)$

Solución en el tiempo para $x_2(t)$:

$x_2(t) = 50 + 100e^{-t}\cos(3t) + \dfrac{400}{3}e^{-t}\sin(3t)$
$x_2(t) = 50 + 100e^{-t}\cos(3t) + 133.33e^{-t}\sin(3t)$

*SIMULINK*

 <p align="center">
   <img src="images/plantilla/imagen_2025-04-12_165408030.png" alt="SITEMA DE BLOQUES" width="600" height="400">
</p>


<div align="center" style="display: flex; justify-content: center; gap: 20px;">

  <img src="images/plantilla/X1.png" alt="X1" width="400" height="200">

  <img src="images/plantilla/X2.png" alt="X2" width="400" height="200">
</div>

*OD45*

```
clc; clear;

% Parámetros
k1 = 0.2; 
k2 = 0.3; 
b  = 0.1; 
m1 = 10; 
m2 = 5; 
g  = 9.81; 
u  = 500; 

% Tiempo integración
tspan = (0:0.01:5);

% Condiciones Iniciales: [x1(0), v1(0), x2(0), v2(0)]
y0 = [0; 0; 0; 0]; 

% Solver
[t, y] = ode45(@miODE, tspan, y0);

% Graficar
plot(t, y(:,1), 'r', 'LineWidth', 1.5); hold on; % x1
plot(t, y(:,3), 'b', 'LineWidth', 1.5);          % x2
legend('x1', 'x2');
xlabel('Tiempo (s)');
ylabel('Posiciones (x)');
title('Sistema de 2 masas, resortes y amortiguador');
grid on;

% EDO
function dy = miODE(t, y)
    % Parámetros dentro de la función
    k1 = 0.2; 
    k2 = 0.3; 
    b  = 0.1; 
    m1 = 10; 
    m2 = 5; 
    g  = 9.81; 
    u  = 500; 

    % Variables
    x1 = y(1);
    v1 = y(2);
    x2 = y(3);
    v2 = y(4);

    % Ecuaciones
    dx1 = v1;
    dv1 = ((-k1 + k2)*x1 - b*v1 - k2*x2 + m1*g) / m1;
    dx2 = v2;
    dv2 = (-k2*x1 + k2*x2 + m2*g + u) / m2;

    dy = [dx1; dv1; dx2; dv2];
end
}
```
<p align="center">
   <img src="images/plantilla/FIGURAODE45.png" alt="OD 45" width="600" height="400">
</p>







## 2. SISTEMA ROTACIONAL

>🔑 *Sistema Rotacional:* Al igual que los sistemas mecánicos, que se rigen por principios físicos fundamentales, en este caso también nos encontramos ante un fenómeno físico. Sin embargo, la diferencia radica en la naturaleza del movimiento, ya que en lugar de tratarse de un desplazamiento lineal, ahora estamos frente a un movimiento de tipo angular. Es decir, en lugar de que un cuerpo se traslade en línea recta, experimenta una rotación alrededor de un eje, lo que implica la intervención de magnitudes como el momento de inercia, el torque y la velocidad angular.

### 2.1 LEYES
Las leyes que rigen estos tipos de sistemas son:
 FUERZA DE TORSION  

 $F_{R}=k*\varphi$ donde $\varphi$ es un angulo de torsion

FUERZA DE FRICCION

 $F_{F}=b\left(\frac{d\varphi}{dt}\right)$ donde $\frac{d\varphi }{dt}$ es la velocidad angular

 TORQUE
 >Es una medida de la fuerza que hace girar un objeto alrededor de un eje o punto. Se calcula multiplicando la fuerza aplicada por la distancia al eje de giro.

 $T=J(\frac{d^{2}\varphi}{dt^{2}})$ donde J es el movimiento de inercia
 
 ### 2.2 ANALISIS
 <p align="center">
   <img src="images/plantilla/imagen_2025-03-31_122007381.png" alt="SISTEMA ROTACIONAL" width="500" height="200">
</p>



Tomando el sentido de T como positivo,nos queda el planteamiento de la suma de fuerzas de tal manera:

$T-F_{R}-F_{F}=J\alpha $ donde $\alpha $ es la acelaracion angular

 Si la fuerza de torsion no es significativa:
 
 $T-F_{F}=J\alpha$

Y ahora utilizamos nuestras ecuaciones auxiliares para reemplazar y expresar todo en términos de una única variable.

$T(t)-k\theta(t)-b\left ( \frac{d\theta (t)}{dt} \right )= J\left ( \frac{d^{2}\theta (t)}{dt^{2}} \right )$
## 3. TRABAJO Y ENERGIAS
 ### 3.1 Trabajo
  >El trabajo es una medida de la realización de un esfuerzo mediante la aplicación de una fuerza que provoca un desplazamiento.

$$W=F_{x}[N*m]$$

Donde definimos en trabajo total realizado como $\int_{0}^{x}kxdx=\frac{1}{2}kx$

### 3.2 Energia y Potencia

 > *Energia* Es la capacidad de un sistema para realizar trabajo, manifestándose principalmente en dos formas: energía cinética, asociada al movimiento, y energía potencial, relacionada con la posición o configuración de un objeto dentro de un campo de fuerzas.
 >*Potencia*  Es la cantidad de trabajo realizado o energía transferida en un determinado período de tiempo. Indica qué tan rápido se realiza un trabajo o se transforma la energía en un sistema y se mide en vatios (W)
 #### 3.2.1 Energia Potencial:
  >La energía potencial es la energía que un objeto tiene debido a su posición o estado, como un resorte comprimido o un objeto elevado sobre el suelo.
 
 Se expresa de tal forma:

$$U= \int_{0}^{h}mgdx=mgh$$

 #### 3.2.2 Energia Cinetica:
  >La energía cinética es la energía que tiene un objeto debido a su movimiento. Cuanto más rápido se mueve el objeto y mayor sea su masa, más energía cinética posee. Esta energía se libera cuando el objeto se detiene o cambia su velocidad.

Y se expresa de tal forma para sistemas lineales:

$T= \frac{1}{2} mv^{2}$

Y para sistemas rotacionales:
 $T= \frac{1}{2}J\dot{\theta }^{2}$

Un cambio en la energía cinética de un objeto ocurre cuando una fuerza realiza trabajo sobre él, ya sea acelerándolo o desacelerándolo. Esta fuerza provoca una variación en la velocidad del objeto, lo que resulta en un aumento o disminución de su energía cinética. Este concepto está relacionado con el teorema del trabajo y la energía.

$\Delta T= \Delta W = \int_{x1}^{x2} F dx$ evaluamos en funcion al tiempo :

$\int_{t1}^{t2} F\frac{dx}{dt}dt$ como $\frac{dx}{dt}= v$ reemplazamos:

$\int_{t1}^{t2}Fvdt$

nose

$\int_{t1}^{t2}m\dot{v}vdt$
Dandonos como resultado en sistemas mecanicos:

$\int_{v1}^{v2}mvdv= \frac{1}{2}mv_{2}^{2}-\frac{1}{2}mv_{1}^{2}$

Dandonos como resultado en sistemas rotacionales:

$$\Delta T= \frac{1}{2}J\dot{\theta _{2}^{2}}-\frac{1}{2}J\dot{\theta _{1}^{2}}$$
#### 3.2.3 Potencia
Como dijimos anteriormente es la variacion del trabajo respecto al tiempo, quedandonos expresadosde tal forma:

$$P=\frac{dW}{dt}$$

Y expresamos la potencia media como: 
$$P_{media}=\frac{W_{realizado}(t_{2}-t_{1})}{(t_{2}-t_{1})}$$

## 4. Aplicando a sistemas mecanicos 
### 4.1 Resorte

<p align="center">
  <img src="images/plantilla/resorte.png" alt=RESORTE" width="200">
</p>

Tenemos  que

$$u= \int_{0}^{x}Fdx$$

Aplicando ley de hooke ya que hablamos de resortes $u= \int_{0}^{x}Kxdx$ 

Evaluando la integral teniendo en cuenta K como constante $k[\frac{x^{2}}{2}]_{0}^{x}$

Nos queda que $u= \frac{1}{2}kx^{2}$

Y aplicando lo mismo para EL CAMBIO DE ENERGIA nos da que :

$\Delta u= \int_{x_{1}}^{x_{2}}Fdx = \int_{x_1}^{x_2}Kxdx = K [\frac{x^{2}}{2}]_{x_1}^{x_2}$

$\Delta u= \frac{1}{2}kx_{1}^{2}-\frac{1}{2}kx_{2}^{1}$

*POTENCIA EN UN RESORTE*

Sabemos que la potencia es definida como la variacion del trabajo con respecto al tiempo

$P= \frac{dW}{dt}= \frac{Fdx}{dt}$ 

Sabiendo que $\frac{dx}{dt}=\dot{x}$ Tenemos que $P = F\dot{x}$ Y remplazando con ley de hooke y derivando $P= kx\dot{x}$ 

Retomando que $u= \frac{1}{2}kx^{2}$ Tenemos que:

$u= \frac{1}{2}kx^{2}$ Derivamos $u=\frac{1}{2}2kx\dot{x}= kx\dot{x}= P$
### 4.2 Masa
*POTENCIA EN UNA MASA*

La cantidad de potencia necesaria para acelerar una masa en movimiento rectilíneo es equivalente a:

$$ P=m\ddot{x}\dot{x}$$

Considerando que $T= \frac{1}{2}mv^{2}$ representa la energía cinética de la masa, obtenemos que:

$$P=m\ddot{x}\dot{x}-m\dot{v}v=\dot{T}$$
### 4.3 Amortiguador
*ENERGIA DISIPADA*

La energía que se pierde en un amortiguador equivale al trabajo neto efectuado sobre él:

$\Delta w= \int_{x1}^{x2}Fdx= \int_{x1}^{x2}b\dot{x}dx$

Respecto al tiempo tenemos que(por $\frac{dt}{dt}$)

$b\int_{t1}^{t2}\dot{x}\frac{dx}{dt}dt= b\int_{t1}^{t2}\dot{x^{2}}dt$

*no importa el signo de la velocidad* ($\dot{x}$)
 *POTENCIA DISIPADA*

 La potencia que se disipa debido a las fuerzas de amortiguamiento en el cilindro corresponde a:

 $$P= \frac{dw}{dt}= F\frac{dx}{dt}= F\dot{x}$$

 Teniendo en cuenta que $F=b\dot{x}$ decimos que $P=b\dot{x}$

## 5. SISTEMAS CONSERVATIVOS
>Un sistema conservativo es aquel en el que la energía total (como la suma de energía cinética y potencial) se mantiene constante a lo largo del tiempo, ya que no hay pérdida de energía por efectos como la fricción o el rozamiento.

Sabemos que toda la energía (cinética y potencial) sale del sistema en forma de trabajo mecánico:

$\Delta (T+u)=\Delta w$

Si no entra energía externa al sistema, entonces la suma de la energía cinética (T) y la energía potencial (U) se mantiene constante.

 $\Delta (T+u)= 0$

 EJEMPLO:
 <p align="center">
   <img src="images/plantilla/EJEMPLO.jpg" alt="SISTEMA" width="500" height="200">
</p>

Ya que trabajamos con sistemas conservativos, decimos que si no hay fricción, la disipación de energía se desprecia.

Siendo el planteamiento de ecuaciones de tal forma:

$$T+u= \frac{1}{2}m\dot{x^{2}}+\frac{1}{2}kx^{2}= CONSTANTE$$

AL momento de derivar nos da que:
 $$\frac{d}{dt}(T+u)= m\dot{x}\ddot{x}+k\dot{x}x$$

Como es conservativo $\Delta (T+u)= 0$

$0= m\dot{x}\ddot{x}+k\dot{x}x$

Y factorizamos $\dot{x}$

$(m\ddot{x}+kx)\dot{x}=0$

Para mantener el sistema conservativo alguno de los terminos ya sea ($(m\ddot{x}+kx)$) o ($\dot{x}$) tienen que ser 0, asi que por facilidad decimos que :

$$m\ddot{x}+kx=0$$

## 3. Subsecciones
Las subsecciones pueden utilizarse para sub dividir ciertos temas que se tienen en clases, por ejemplo si se está trabajandolos conversores D/A, puede ser necesario subdividir este en circuito de resistencias ponderadas y circuito de escalera R2R. 
### 3.1. Título de subsecciones
Para la creación de estas subsecciones debe utilizar un tamaño de letra más pequeño, por lo tanto utilice la etiqueta '###' 
### 3.2. Numeración de subsecciones
Siga la numeración de la sección seguida de un punto y luego el número de la subsección.

## 4. Ejemplos
Si en algún caso pretende dar un ejemplo explicativo ya sea a través de texto o através de ecuaciones matemáticos, utilizar la palabra 'Ejemplo' seguido de una numeración consecutiva dentro de la clase. Utilice el emoji 💡 antecediendo la palabra.

## 5. Ecuaciones
Para la edición de ecuaciones debe utilizar la etiqueta '$$' al comienzo y final de la ecuación para que la ecuación quede centrada ocupando una línea. Si se quiere que la ecuación quede integrada en el texto debe utilizar la etiqueta '$' al comienzo y final de la ecuación. Las ecuaciones pueden ser editadas utilizando el código LATEX, en el siguiente enlace encuentran un editor de ecuaciones que les genera el código. http://www.alciro.org/tools/matematicas/editor-ecuaciones.jsp . Sin embargo hay muchas otras herramientas que pueden utilizar para esto.

💡**Ejemplo 1:** si se va a representar la ecuación de la ley de Ohm se puede mostrar así $R=\frac{V}{I}$ o también,

$$R=\frac{V}{I}$$

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
