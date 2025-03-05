# Ejercicio Raices Reales Diferentes y Raices Reales Iguales y Explicacion de la SOLUCION RESUMIDA
De acuerdo a nuestra clase #4 vimos el tema de Raices Reales Diferentes y Raices Reales Iguales, comenzando esta clase con un ejercicio del tema y luego la explicacion y solucion del tema SOLUCION RESUMIDA.
## 1. Ejercicio Raices Reales Iguales y Raices Reales Diferentes
Se inicia la clase con el siguiente ejercicio: 

$$G(s)=\frac{2s-3}{(s+2)(s+10)^{3}}$$

Al analizar el ejercicio nos damos cuenta que es un problema que contiene raices reales diferentes e iguales a al vez, por lo cual comenzamos planteando las fracciones parciales para luego poder aplicar los dos metodos mencionados anteriormente.

Ya que el termino $(s+10)^{3}$ hace parte de raices reales iguales debemos tener en cuenta su formulacion en las fracciones parciales siendo que:  

$$ G(s)=\frac{A}{(s+2)}+\frac{B}{(s+10)^{3}}+\frac{C}{(s+10)^{2}}+\frac{D}{(s+10)}$$

Utilizamos el metodo de Raices Reales Diferentes para encontrar el valor de la variable A:

$A=\left [ \frac{(s+2)(2s-3)}{(s+2)(s+10)^{3}} \right ]\,s=-2$

$A=\left [ \frac{(-2+2)(2(-2)-3}{(-2+2)(-2+10)^{3}} \right ]\$

$A=\left [ \frac{-7}{(8)^{3}} \right]\$

$A= \frac{-7}{512}$

Ahora para la variable B usamos el metodo de Raices Reales Iguales

$$B=\left [ \frac{(s+10)^{3}(2s-3)}{(s+2)(s+10)^{3}} \right ], s=-10$$

$B=\left [ \frac{(-10+10)^{3}(2(-10)-3)}{(-10+2)(-10+10)^{3}} \right ]$

$B=\frac{23}{8}$

$$C=\frac{d}{ds}\left [ \frac{(s+10)^{3}(2s-3)}{(s+2)(s+10)^{3}} \right ],s=-10$$

Utilizando 

![Derivada de un cociente](images/plantilla/derivada.png)

Tenemos que: 
 $C=\left [ \frac{2(s+2)-(2s-3)(1)}{(s+2)^{2}} \right ],s=-10$

 $C=\left [ \frac{2((-10)+2)-(2(-10)-3)(1)}{((-10)+2)^{2}} \right ]$

 $C=\left [ \frac{-16+23}{64} \right ]=\frac{7}{64}$

Y por ultimo paar la variable D, hacemos lo mismo, la derivada de la ecuacion anterior o la  doble derivada de la primera ecuacion:

$$D=\frac{d}{ds}\left [ \frac{2(s+2)-(2s-3)(1)}{(s+2)^{2}} \right ],s=-10$$

$D=\left [ \frac{(2-2)(s+2)^{2}-2(s+2)(2(s+2))-(2s-3)}{(s+2)^{4}} \right ],s=-10$

$D=\left [ \frac{(2-2)((-10)+2)^{2}-2((-10)+2)(2((-10)+2))-(2(-10)-3)}{((-10)+2)^{4}} \right ]$

$D=\frac{-112}{4096}$

Al final tendriamos que:

$$G(s)=\frac{\frac{-7}{512}}{(s+2)}+\frac{\frac{23}{8}}{(s+10)^{3}}+\frac{\frac{7}{64}}{(s+10)^{2}}+\frac{\frac{-112}{4096}}{(s+10)}$$

## 2. Solucion Resumida 
Se usa este caso cuando encontramos polinomios de segundo grado en los factores del denominador, coemnzamos con un ejercicio en clase:

$$G(s)=\frac{s^{2}+2s+3}{(s^{2}+2s+2)(s^{2}+2s+5)}$$

Primero tenemos que resolver los factores de segundo grado ya sea si es posible por metodos de factorizacion, si no por medio de la ecuacion cuadratica:

$x=\frac{-b\frac{+}{}\sqrt{b^{2}-4ac}}{2a}$

Y tenemos dos factores

### 1.1 $(s^{2}+2s+2)$
a=1 , b= 2, c=2

$x=\frac{-2 \frac{+}{}\sqrt{2^{2}-4(1)(2)}}{2(1)}$

$x=\frac{-2 \frac{+}{}\sqrt{4-8}}{2}$

$x=\frac{-2 \frac{+}{}\sqrt{-4}}{2}$

Como la raiz de -4 no existe en los numeros reales pasamos a resolver mediante numeros complejos, usando el valor de $i=\sqrt{-1}$ , quedando de tal forma:

$$x=\frac{-2\frac{+}{}\sqrt{4}i}{2}$$

$$x=-1\frac{+}{}i$$

 ### 1.2 $(s^{2}+2s+5)$

a=1, b=2 , c=5
$x=\frac{-2 \frac{+}{}\sqrt{2^{2}-4(1)(5)}}{2(1)}$

$x=\frac{-2 \frac{+}{}\sqrt{4-20}}{2}$

$x=\frac{-2 \frac{+}{}\sqrt{-16}}{2}$

Volvemos a usar el termino de i

$$x=\frac{-2\frac{+}{}\sqrt{16}i}{2}$$

$$x=-1\frac{+}{}2i$$

Teniendo estos factores separamos en fracciones parciales de la siguiente forma: 

$$G(s)=\frac{As+B}{(s^{2}+2s+2)}+\frac{Cs+D}{s^{2}+2s+5}$$

Y escribimos igualando las dos ecuaciones:

$$G(s)=\frac{s^{2}+2s+3}{(s^{2}+2s+2)(s^{2}+2s+5)}=\frac{As+B}{(s^{2}+2s+2)}+\frac{Cs+D}{s^{2}+2s+5}$$

Multiplicamos uno de los factores de segundo orden, elegimos el factor de $(s^{2}+2s+2)$ y evaluando s en los resultados de la solucion de la cuadratica quedando de tal manera:

$\left [ G(s)=\frac{(s^{2}+2s+2)(s^{2}+2s+3)}{(s^{2}+2s+2)(s^{2}+2s+5)}=\frac{(s^{2}+2s+2)As+B}{(s^{2}+2s+2)}+\frac{(s^{2}+2s+2)Cs+D}{s^{2}+2s+5} \right ] s=-1+j$

Simplificamos terminos reemplazando por el valor de s, quedando de tal manera: 

$G(s)=\frac{(s^{2}+2s+3)}{(s^{2}+2s+5)}={As+B}+(0), s=-1+j$

$G(s)=\frac{((1+j-j^{2})+2(1+j)+3)}{(1+j-j^{2})+2(1+j)+5)}={A(1+j)+B}$

$G(s)=\frac{((-1+j)^{2}+2(-1+j)+3)}{((-1+j)^{2}+2(-1+j)+5)}={A(-1+j)+B}$

Y resolvemos multiplicaciones

$G(s)=\frac{1-2j+j^{2}-2+2j+3}{1-2j+j^{2}+2j+5}$

Simplificamos y teniendo en cuenta que $j^{2}=-1$ tendriamos que: 

$G(s)=\frac{1-1-2+3}{1-1-2+5}={A+Aj+B}$

$G(s)=\frac{1}{3}$

Separamos los sistemas de ecuaciones para asi resolver el sistema, teniendo en cuenta la parte real y la parte imaginaria:

$\frac{1}{3}=-A+Aj+B$

$Aj=0 , A=0, B=\frac{1}{3}$


Para las variables C y D hacemos el mismo procedimiento pero con el otro factor cuadratico:

$G(s)=\frac{(s^{2}+2s+5)(s^{2}+2s+3)}{(s^{2}+2s+2)(s^{2}+2s+5)}=\frac{(Cs+D)s^{2}+2s+5}{(s^{2}+2s+5)}, s=-1+2j$

Simplificamos

$\frac{(s^{2}+2s+3)}{(s^{2}+2s+2)}=(Cs+D), s=-1+2j$

Resolvemos

$\frac{((-1+2j)^{2}+2(-1+2j)+3)}{((-1+2j)^{2}+2(-1+2j)+2)}=(C(-1+2j)+D)$

$\frac{-1-4j+4j^{2}-2+4j+3}{-1-4j+4j^{2}-2+4j+2}=-C+2Cj+D$

Simplificamos y teniendo en cuenta que $j^{2}=-1$ tendriamos que: 

$\frac{2}{3}=-C+2Cj+D$

Separamos los sistemas de ecuaciones para asi resolver el sistema, teniendo en cuenta la parte real y la parte imaginaria:

$\frac{2}{3}=-C+2Cj+D$

$ 2Cj=0 , C=0 $

$\frac{2}{3}=-C+D$

$D=\frac{2}{3}$

## 9. Ejercicios
📚 Ejercicio #1

$$ \frac{2x^{2}+4x+22}{x^{2}+2x+10}=\frac{ax+b}{x^{2}+2x+10}=6$$

$x=\frac{-b\frac{+}{}\sqrt{b^{2-4ac}}}{2a}=\frac{-2\frac{+}{}\sqrt{4-4(1)(10)}}{2(1)}$

$=\frac{-2\frac{+}{}\sqrt{36}}{2}==\frac{-2\frac{+}{}\sqrt{36i}}{2}=\frac{-2\frac{+}{}6i}{2}=-1\frac{+}{}3i$

$[\frac{(x^{2}+2x+10)(2x^{2}+4x+22)}{(x^{2}+2x+10)}=\frac{(x^{2}+2x+10)As+B}{(x^{2}+2x+10)}]$

$[2x^{2}+4x+22],{s=-1+3j}=[As+B],{s=-1+3j}$

$2(-1+3j)^{2}+4(-1+3j)+22=A(-1+3j)+B$

$2(1+6j+9j^{2})-4+12j+22=-A+3Aj+B$

$2(1+6j+9)-4+12j+22=-A+3Aj+B$

$2-12j-18-4+12j+22=-A+3Aj+B$

$-18+20=-A+3Aj+B$

$2=-A+3Aj+B$

$3Aj=0, A=0$

$2=-A+B\mapsto B=2$

$G(x)=\frac{As+B}{x^{2}+2x+10}\mapsto \frac{2}{x^{2}+2x+10}$

$G(s)=\frac{2}{x^{2}+2x+10}$

📚 Ejercicio #2

$$\frac{x-5}{(x^{2}+2x+5)(x^{2}+6x+10)}=\frac{Ax+B}{(x^{2}+2x+5)}+\frac{Cx+D}{(x^{2}+6x+10)}$$

$x^{2}+2x+5\to \frac{-2\frac{+}{}\sqrt{4-4(1)(5)}}{2}=\frac{-2\frac{+}{}\sqrt{4-20}}{2}$

$\frac{-2\frac{+}{}\sqrt{-16}}{2}\to \frac{-2\frac{+}{}4i}{2}=-1\frac{+}{}2i$

$x^{2}+5x+10\to \frac{-6\frac{+}{}\sqrt{36-4(10)(1)}}{2}=\frac{-6\frac{+}{}\sqrt{-4}}{2}$

$\frac{-6\frac{+}{2i}}{2}\to -13\frac{+}{}i$

$[\frac{(x^{2}+2x+5)(x-5)}{(x^{2}+2x+5)(x^{2}+6x+10)}=\frac{(x^{2}+2x+5)Ax+B}{(x^{2}+2x+5)}+\frac{(x^{2}+2x+5)Cx+D}{(x^{2}+6x+10)}]$

$[\frac{x-5}{x^{2}+6x+10}],x=-1+2j  =[Ax+B],x=-1+2j ,x=-1+2j $

$\frac{(-1+2j)+5}{(-1+2j)^{2}+6(-1+2j)+10}=A(-1+2j)+B$

$\frac{2j+4}{1-4j+4j^{2}-6+12j+10}=-A+2Aj+B$

$\frac{2j+4}{8j+1}=-A+2Aj+B$

$\frac{2j+4}{1+8j}*\frac{1-8j}{1-8j}=\frac{2j+16+4-32j}{1+64}$

$\frac{-30j+20}{65}=\frac{-30}{65}+\frac{20}{65}=-A+2Aj+B$

$2Aj=\frac{-30j}{65}\to 2A=\frac{-30}{65}\to A=\frac{\frac{-30}{65}}{\frac{2}{1}}=\frac{-30}{130}$

$$A=\frac{-3}{13}$$

$\frac{20}{65}=-A+B,\frac{20}{65}=\frac{3}{13}+B$

$B=\frac{20}{65}-\frac{3}{13}=\frac{260-195}{845}=\frac{65}{45}=\frac{5}{65}$

$$B=\frac{1}{13}$$

Multiplicar todo por $(x^{2}+6x+10)$

$[\frac{(x-5)}{(x^{2}+2x+5)}=Cx+D],x=-3+j$

$\frac{((-3+j)-5)}{(-3+j)^{2}+2(-3+j)+5}C(-3+j)+D$

$\frac{-8+j}{9-6j-1-6+2j+5}=-3C+Cj+D$

$\frac{-8+j}{-4j+7}=-3C+Cj+D$

$\frac{-8+j}{7-4j}*\frac{7+4j}{7+4j}=\frac{-56-32j+7j-4}{49+16}$

$\frac{-60-25j}{65}=-3C+Cj+D$

$\frac{-60}{65}-\frac{25j}{65}=-3C+Cj+D$

$Cj=\frac{-25j}{65}, C=\frac{-25}{65}=\frac{-5}{13}$

$-3C+D=\frac{-60}{65},-3(\frac{-5}{13})+D=\frac{-60}{65}$

$\frac{15}{13}+D=\frac{-60}{65},D=\frac{-60}{65}-\frac{15}{13}=\frac{-780-975}{845}=\frac{-1755}{545}=\frac{-135}{65}=\frac{-27}{13}$

$$G(x)=\frac{x(\frac{-3}{13})+\frac{1}{3}}{(x^{2}+2x+5)}+\frac{(\frac{-5}{13})x-\frac{27}{13}}{(x^{2}+6x+10)}$$



## 10. Conclusiones
En la clase se abordaron los métodos para resolver fracciones parciales con raíces reales diferentes e iguales. Se aplicaron estos conceptos a ejercicios específicos, descomponiendo funciones en términos parciales y utilizando derivadas para determinar coeficientes. Además, se explicó la solución resumida cuando aparecen factores cuadráticos en el denominador, empleando números complejos y sistemas de ecuaciones. Estos métodos permiten simplificar expresiones racionales para su análisis y resolución en contextos de sistemas dinámicos y transformadas de Laplace.

## 11. Referencias
-OpenStax. (s.f.). Cálculo, Volumen 2 (Sección 3.4: Fracciones parciales). Recuperado el [fecha de acceso], de https://openstax.org/books/c%C3%A1lculo-volumen-2/pages/3-4-fracciones-parciales
