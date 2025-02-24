# USO DE MATLAB PARA EL DESARROLLO DE LA TRANSFORMADA INVERSA
El objetivo de la clase es solucionar la transformada inversa utilizando los metodos de raices reales diferentes, y raices reales iguales, y comprobarlos en la herramienta MATLAB con el fin de corroborar los resultados realizados de manera manual.  
# 1. Conceptos
> 🔑 MATLAB es una herramienta muy útil para realizar transformadas de Laplace, tanto simbólicas como numéricas. Para trabajar con la transformada de Laplace en MATLAB, generalmente se utiliza la caja de herramientas Symbolic Math Toolbox.

> 🔑 Una ecuación diferencial es una ecuación que relaciona una función con sus derivadas, describiendo cómo cambia una cantidad en función de otra.

> 🔑 Las raíces reales diferentes son los valores distintos de s en los que una función de Laplace se anula. Se utilizan para descomponer la transformada de Laplace y hallar su inversa a través de fracciones parciales.

> 🔑 El método de raíces reales iguales es una técnica utilizada para hallar la transformada de Laplace de una función dada, especialmente cuando el denominador de la función está factorizado en términos de raíces repetidas (o iguales) en el dominio del tiempo.

## 2. Transformada inversa de Laplace aplicada en MATLAB

En MATLAB, la transformada inversa de Laplace se realiza con la función ilaplace. Esta función toma como entrada una expresión en 𝑠 (la variable del dominio de Laplace), y devuelve la expresión equivalente en el dominio del tiempo 

## 3. Uso básico de la transformada inversa de Laplace en MATLAB:

El procedimiento más sencillo se trata de utilizar la función ilaplace para calcular la transformada inversa de una función en el dominio de s.

## 3.1. Definir variables simbólicas

Definir las variables simbólicas para s (dominio de Laplace) y t (dominio del tiempo).
syms t s

## 3.2. Definir la función: 
Definir la función en el dominio de Laplace (en términos de s).

$$F_s = 1 / (s + 1);$$

## 3.3. Calcular la transformada inversa la place

$$f_t = ilaplace(F_s, s, t);$$

## 3.3. Mostrar el resultado

$$disp('La transformada inversa de Laplace de F(s) es:');$$
$$disp(f_t);$$

## 4. Explicacion

## 4.1. Definir las variables simbólicas:

syms s t permite definir 𝑠 y 𝑡 

## 4.2. Definir la función en 𝑠:

F_s = 1 / (s + 1) es la función que estamos transformando. En este caso, es una función simple.

## 4.3. Calcular la transformada inversa:

ilaplace(F_s, s, t) aplica la transformada inversa de Laplace a la función 𝐹(𝑠), donde:

F_s es la función en el dominio de s,
s es la variable de Laplace,
t es la variable en el dominio del tiempo.

## 4.4. Mostrar el resultado

El resultado de la transformada inversa se almacena en f_t y se muestra en la ventana de comandos de MATLAB.

Resultado esperado:

La transformada inversa de $F\left(s\right)=\frac{1}{\left(s&plus;1\right)}$ es:

$$f\left(t\right)=e^{-t}$$

## 💡5. Ejemplo

Obtenga la transformada inversa utilizando el metodo de raices reales diferentes, de:

$$f\left(S\right)=\frac{s&plus;3}{(s&plus;1)(s&plus;2)}$$

utilizamos la siguiente formula:

$$a\left(k\right)=\left[\left(s&plus;pk\right)\left(\frac{A(s)}{B(s)}\right)\right]_{s=-pk}$$

ahora:

$f\left(S\right)=\frac{s&plus;3}{(s&plus;1)(s&plus;2)}=\frac{A(s)}{B(s)}$

y:

$f(S)=\frac{A}{S&plus;1}&plus;\frac{B}{S&plus;2}=\frac{S&plus;3}{(S&plus;1)(S&plus;2)}$

solucionamos A:

$[A=\left[\frac{(s&plus;1)(s&plus;3)}{(s&plus;1)(s&plus;2)}\right]s=-1]$ 

$A=\frac{-1&plus;3}{-1&plus;2}=2$

Solucionamos B:

$B=\left[\frac{(s&plus;2)(s&plus;3)}{(s&plus;1)(s&plus;2)}\right]s=-2$

$B=\frac{-2&plus;3}{-2&plus;1}=\frac{1}{-1}=-1$

Hallando A y B tenemos el resultado:

$$[L^{-1}\left[\frac{2}{s&plus;1}&plus;\frac{1}{s&plus;2}\right]=2e^{-t}-e^{-2t}]$$

CASO 2: raices reales iguales

FORMULA:

$[f(s)=\frac{A(s)}{B(s)}=\frac{b_{3}}{(s&plus;1)^{3}}&plus;\frac{b_{2}}{(s&plus;1)^{2}}&plus;\frac{b^{_{1}}}{(s&plus;1)}]$

$[(s&plus;1)^{3}\frac{A(s)}{B(s)}=\frac{b_{3}(s&plus;1)^{3}}{(s&plus;1)^{3}}&plus;\frac{b_{2}(s&plus;1)^{3}}{(s&plus;1)^{2}}&plus;\frac{b_{1}(s&plus;1)^{3}}{s&plus;1}]$

$\left[(s&plus;1)^{3}\frac{A(s)}{B(s)}\right]_{s=-1}$

ahora

$\left[(s&plus;1)^{3}\frac{A(s)}{B(s)}\right]_{s=-1}$

$=\left[b_{3}&plus;b_{2}(s&plus;1)&plus;b_{1}(s&plus;1)^{2}\right]_{s=-1}$

$\left[(s&plus;1)^{3}\frac{A(s)}{B(s)}\right]_{s=-1}$

$=b_{3}$

Ejemplo

Obtenga la transformada inversa de:

$G=\frac{3}{(s&plus;5)(s&plus;8)^{3}}=\frac{A}{s&plus;5}&plus;\frac{B}{(s&plus;8)^{3}}&plus;\frac{C}{(s&plus;8)^{2}}&plus;\frac{D}{(s&plus;8)}$

$A=\left[(s&plus;5)\frac{3}{(s&plus;5)(s&plus;8)^{3}}\right]_{s-5}$

$A=\frac{3}{(-5&plus;8)^{3}}=\frac{3}{27}=\frac{1}{9}$

ahora

$B=\left[(s&plus;8)^{3}\frac{3}{(s&plus;5)(s&plus;8)^{3}}\right]_{s=-8}$

$B=\frac{3}{-8&plus;5}=-1$

$C=\frac{d}{ds}\left[(s&plus;8)^{3}\frac{3}{(s&plus;5)(s&plus;8)^{3}}\right]_{s=-8}$

ahora

$\frac{d}{ds}(\frac{3}{s&plus;5})_{s=-8}=\left[\frac{0(s&plus;5)-3(1)}{(s&plus;2)^{2}}\right]_{s=-8}$

$B=\frac{-3}{9}=\frac{-1}{3}$

$D=\frac{d^{2}}{ds^{2}}=\left[(s&plus;8)^{3}\frac{3}{(s&plus;5)(s&plus;8)^{3}}\right]_{s=-8}$

$D=\frac{d^{2}}{ds^{2}}=\left[(s&plus;8)^{3}\frac{3}{(s&plus;5)(s&plus;8)^{3}}\right]_{s=-8}=[\frac{0(s&plus;5)^{2}&plus;3&plus;(2(s&plus;5))}{(s&plus;5)^{4}}]_{_{s=-8}}$

$[=\frac{-18}{81}=\frac{-2}{9}]$

$L^{-1}\left[\frac{1/9}{s&plus;5}-\frac{1}{(s&plus;8)^{3}}-\frac{1/3}{(s&plus;8)^{2}}-\frac{2/9}{s&plus;8}\right]=\frac{1}{9}e^{-st}-e$

Ejercicio:

$G=\frac{25*3}{(s&plus;2)(s&plus;10)^{3}}=\frac{A}{(s&plus;2)}&plus;\frac{B}{(s&plus;10)^{3}}&plus;\frac{C}{(s&plus;10)^{2}}&plus;\frac{D}{(s&plus;10)}$

$A=\left[\frac{(s&plus;2)(25-3)}{(s&plus;2)(s&plus;10)^{3}}\right]_{s=-2}=\frac{-7}{512}$

$B=\left[(s&plus;10)^{3}\frac{25-3}{(s&plus;2)(s&plus;10)^{3}}\right]_{s=-10}=\frac{23}{8}$

$[C=\frac{d}{ds}\left[\frac{(s&plus;10)^{3}(25-3)}{(s&plus;2)(s&plus;10)^{3}}\right]_{s=-10}=\frac{d}{ds}\left[\frac{25-3}{s&plus;2}\right]]$

$\left(\frac{2(s&plus;2)-(25-3)}{(s&plus;2)^{2}}\right)_{s=-10}=\left(\frac{2(-10&plus;2)-(-20-3)}{(-10&plus;2)^{2}}\right)=\frac{17}{64}$

$D=\frac{d^{2}}{dd^{2}}=\left[\frac{2(s&plus;2)-1(25-3)}{(s&plus;2)^{2}}\right]_{s=-10}$

$\left[\frac{(2-2)(s&plus;2)^{2}-2(s&plus;2)(2(s&plus;2))-(25-3)}{(s&plus;2)^{4}}\right]_{s=-10}=\frac{-112}{4096}$










## 8. Conclusiones
En conclusión, la clase explicó qué son los sistemas dinámicos y cómo se pueden estudiar usando modelos matemáticos y ecuaciones diferenciales. Se diferenciaron los sistemas lineales y no lineales, resaltando la importancia de validar los modelos para que sean precisos. También se repasó la transformada de Laplace y su inversa, herramientas útiles para resolver ecuaciones de manera más sencilla.

## 9. Referencias
Ejercicio 1: Ejemplo formulado por el estudiante.
Ejercicio 2: Platzi. (s.f.). Transformada de Laplace de la derivada de una función - PVI - Repaso. Recuperado el [fecha de consulta], de https://platzi.com/tutoriales/1320-ecuaciones/8937-transformada-de-laplace-de-la-derivada-de-una-funcion-pvi-repaso/
