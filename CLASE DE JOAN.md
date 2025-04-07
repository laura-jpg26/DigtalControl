 # SOLUCIONES DIFERENCIALES ECUACIONES
> Una solución de una ecuación diferencial es una función f definida en un intervalo S que tiene al menos N derivadas continuas en S y que al sustituirlas en la ecuación diferencial ordinaria de N-ésimo orden reducen la ecuación a la identidad.
 ## 1. METODOLOGIA Y SOLUCION 
 Se aplica la Transformada de la place a toda la ecuación una a una de tal manera que se desarrolle o obtenga una ecuación algebratica en el dominio de S. Se despeja la variable que representa la salida de la ecuación (después del =), se aplica la transformada inversa de la place a la expresión obtenida para hacer la solucion en el dominio del tiempo (ΔT).
 
 $L{{f}\'(t)}=SF(s)-f(0)$
 
 ## 2. EJERCICIOS DE CLASE
 
 EJEMPLO 1 CLASE
 
 $x^{''}+x^{'}+2x=0,      x(0)=a,  x^{'}f(0)=b$
 
 Aplicando transformada de Laplace
 
 $[s^{2}X(s)-sx(0)-x^{'}]+3[sX(s)-x(0)]+2Xs=0$
 
 Reemplazamos condiciones iniciales
 
 $[s^{2}X(s)-as-b]+3[sX(s)-a]+2X(2)=0$
 
 Despejando x
 
 $(s^{2}+3s+2)X(s)=as+b+3a$
 
 Solución Dominio
 
 $X(s=\frac{as+b+3a}{s^{2}+3s+2})=\frac{as+b+3a}{(s+1)(s+2)}=\frac{2a+b}{s+1}-\frac{a+}{s+2}$
 
 $L{f^{''}(t)}=s^{2}F(s)-sf(s)-f^{'}(0)$
 
 $L{f^{''}(t)}=s^{3}F(s)-s^{2}f(0)-s^{'}f(0)-f^{''}(0)$
 
 Aplicando transformada inversa  desde las tablas para volver al dominio del tiempo
 
 $x(t)=L^{-1}[X(s)]=L^{-1}[\frac{2a+b}{s+1}]-L^{-1}[\frac{a+b}{s+2}]$
 
 $x(t)=(2a+b)e^{-t}-(a+b)e^{-2t}              (t>=0)$
 
 ## Ejemplo 2 CLASE
 
 $x^{''}+2x^{'}+5x=3$
 
 $s^{2}x(s)+2sX(s)+5x(s)=3/s$
 
 $Xs(s^{2}+2s+5)=3/s$
 
 $x(s)=\frac{3}{s(s^{2}+2s+5)}$
 
 $x(s)=\frac{A}{s}+\frac{Bs+C}{s^{2}+2s+s}$
 
 Hacemos formula cuadratica para saber cuanto vale s
 
 $r=\frac{-2+-\sqrt{4-(4)(1)(5)}}{2}$
 
 $r=\frac{-2+-\sqrt{-16}}{2}$
 
 $r=\frac{-2+-(-4)}{2}$
 
 $s=-1+-(2i)$
 
 Seguimos con la ecuacion
 
 $A=\frac{3s}{s(s^{2}+2s+5)}\left |s=0...  A=\frac{3}{s} \right |$
 
 $=\frac{3}{s}\left | s=s-1+2i...=Bs+c\right |=s=-1+2i$
 
 $\frac{3}{-1+2i}=-B+2Bi+c$
 
 $\frac{3(-1-2i)}{-1+2i(-1-2i)}=-B+2Bi+C$
 
 $\frac{-3-6i}{1+2i-2i+4}=-B+2Bi+C$
 
 $\frac{-3-6i}{5}=-B+2Bi+C$
 
 $-\frac{6}{5}=2B$
 
 $B=-\frac{6}{10}$
 
 $C=-\frac{3}{5}-\frac{3}{5}=-\frac{6}{5}$
 
 $X(s)=\frac{3/5}{s}-\frac{3/5s-6/5}{s^{2}+2s+5-4+4}$
 
 $\frac{s}{5}\left ( \frac{s+2}{(s+1)^{2}+4} \right )\frac{3}{5}\left ( \frac{s+1}{(s+1)^{2}+4}+\left ( \frac{1}{(s+1)+4} \right )$
 
 $L^{-1}{X(s)}=\frac{3}{5}-\frac{3}{5}e^{-t}cos(2t)-\frac{3}{10}e^{-t}sen(2t)$
 
 ## 3 . EJERCICIOS PROPUESTOS
 
 EJERCCIo 1
 
 $y′′+4y=sin(2t),           y(0)=0,          y′(0)=14$
 
 Aplicamos la Transformada de Laplace a ambos lados
 
 $L{y^{''}}+4L{y}=L{sin(2t)}$
 
 Usamos las transformadas
 
 $L{y^{′′}}=s^{2}Y(s)−sy(0)−y^{'}(0)=s^{2}Y(s)-1$
 
 $L{y}=Y(s)$
 
 $L\left\{sen(2t) \right\}=\frac{2}{s^{2}+4}$
 
 Despejamos Y(s)
 
 $Y(s)=\frac{1+\frac{2}{s^{2}+4}}{s^{2}+4}$
 
 $Y(s)=\frac{1}{s^{2+4}}+\frac{2}{(s^{2}+4)^{2}}$
 
 Aplicamos la transformada inversa de LaPlace
 
 $L^{-1}\left\{ \frac{1}{s^{2}+4}\right\}=\frac{sin(2t)}{2}$
 
 La segunda parte requiere de la formula:
 
 $L^{-1}=\left\{ \frac{2}{(s^{2}+4)^{2}}\right\}=\frac{t}{2}sin(2t)$
 
 Por lo tanto
 
 $y(t)=\frac{sin(2t)}{2}+\frac{t}{2}sin(2t)$
 
 Solucion:
 
 Aplicamos la transformada de Laplace
 
 $L\left\{ y^{''}\right\}-2L\left\{ y^{'}\right\}+2L\left\{ y\right\}=L\left\{ u_{\pi }(t)\right\}$
 
 usamos:
 
 $L\left\{ y^{''}\right\}=s^{2}Y(s)-ys(0)-y^{'}(0)=s^{2}Y(s)-1$
 
 $L\left\{ y^{'}\right\}=sY(s)-y(0)=sY(s)$
 
 $L\left\{ y\right\}=Y(s)$
 
 Y para la funcion escalon:
 
 $L\left\{ u_{\pi }(t)\right\}=\frac{e^{-\pi s}}{s}$
 
 Entonces
 
 $(s^{2}-2s+2s)Y(s)-1=\frac{e^{-\pi s}}{s}$
 
 Despejamos Y(s)
 
 $Y(s)=\frac{1}{s^{2}-2s+2}+\frac{e^{-\pi s}}{s(s^{2}-2s+2)}$
 
 
 Hacemos transformada inversa de Laplace
 
 Primera parte:
 
 $L^{-1}\left\{ \frac{1}{(s-1)^{2}+1}\right\}=e^{t}sin(t)$
 
 
 La segunda requiere descomócision por partes (fraciones parciales y formulas)
 
 $L^{-1}\left\{ \frac{e^{-\pi s}}{s(s^{2}-2s+2)}\right\}=u_{\pi }(t)*g(t-\pi )$
 
 Donde g es la transformada inversa de $\frac{1}{s(s^{2}-2s+2)}$ que se obtiene aplicando la inversa
 Y con esto llegamos a la solucion de la ecuacion
 
 $y(t)=e^{t}sin(t)+u_{\pi }(t)*g(t-\pi )$
 
 
 ## 4. CONCLUSIONES 
 
 Resolver ecuaciones diferenciales es una herramienta clave en matemáticas aplicadas. Gracias a ella, podemos modelar y predecir cómo se comportan distintos fenómenos en campos como la física, la ingeniería, la economía y la biología. Usando métodos tanto analíticos como numéricos, logramos encontrar soluciones que pueden ser exactas o aproximadas, dependiendo de lo complejas que sean las ecuaciones y de cómo se apliquen.
 Técnicas como la separación de variables, el método de los coeficientes indeterminados, la transformada de Laplace, y métodos numéricos como Euler o Runge-Kutta, nos ayudan a resolver problemas que están relacionados con cambios en el tiempo o en el espacio. A esto se le suma que las herramientas computacionales han dado un gran paso para solucionar ecuaciones diferenciales complejas que no se pueden resolver de manera analítica.
 En resumen, estudiar y resolver ecuaciones diferenciales es critical para entender y modelar sistemas dinámicos en el mundo real. Para aplicarlas de manera efectiva, no solo se necesita conocimiento teórico, sino también la habilidad de usar métodos computacionales avanzados que nos ofrezcan resultados precisos y útiles en la práctica.
 
 ## 5. REFERENCIAS
 
 Clase de sistemas dinamicos
 https://www.youtube.com/watch?v=_-v7jWOX2PY
 
