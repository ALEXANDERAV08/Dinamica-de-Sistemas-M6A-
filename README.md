# Dinamica-de-Sistemas-M6A-
# APUNTES DINAMICA DE DISTEMAS PRIMER CORTE 
# TRANSFORMADA DE LAPLACE 
## 1. Sistema
Se define como sistema a una combinacion de componentes que trabajan conjuntamente para alcanzar un objetivo especifico, estos omponentes pueden ser representados mediante reglas o principios que relacionan las salidas con las entradas, siguiendo ciertas reglas o principios que determinan como las entradas se transforman en salidas.
## 2. Sistema Dinamico
Un sistema dinamico es aquel donde lo que sucede ahora (su salida) esta influenciada por lo que ocurrio antes (su entrada) 
si su salida depende solo de la entrada actual, el sistema se conoce como ESTATICO 
En resumen un sistema dinamico es aque donde las salidas estan influenciadas por entradas anteriores, mientras que un sistema que solo responde a las entradas del momento presente se denomina sistema estatico.  
## 3. Planta
Una planta se refiere al conjunto de componentes físicos que permiten ejecutar un proceso, como maquinaria o infraestructura. Este conjunto puede ser descrito mediante modelos matemáticos y representado como uno o varios sistemas interconectados que permiten entender y controlar su comportamiento.
## 4. Proceso
Un proceso es el conjunto de acciones organizadas que permiten crear o desarrollar un producto o alcanzar un objetivo. En el campo del control, a veces se utiliza como equivalente a planta, aunque en un sentido más preciso no son términos intercambiables.
## Transformadade LaPlace
La trnsforma de laplace es una tecnica que transforma funciones que dependen del tiempo en una forma mas simplificada y facil de manejar, especialmente cuando se trabaja con ecuaciones diferenciales, en vez de resolver estas ecuaciones directamente,la transformada de laplace las convierte en ecuaciones algebraicas simples.
basicamente toma una funcion en el tiempo y la transforma el dominio de la frecuencia donde se puede hacer calculos mas sencillos. 

$$\mathcal{L}\{f(t)\} = F(s) = \int_{0}^{\infty} e^{-st} f(t) \, dt$$

## Algunas propiedades
 ### 1. linealidad 
la transformada de laplace de una suma de funciones es igual a la suma de las transformadas de cada funcion

$$\mathcal{L}(\{a f(t) + b g(t)\} = a \mathcal{L}\{f(t)\} + b \mathcal{L}\{g(t)\})$$

donde a y b son constantes.

### 2. Transformada de la derivada
La transforma de laplace de la primera derivada de una funsion es:


 $$\mathcal{L}\{f'(t)\} = s F(s) - f(0)$$

Para la segunda derivada:

$$\mathcal{L}\{f''(t)\} = s^2 F(s) - s f(0) - f'(0)$$

## 3. escalon unitario
la transformada de laplas de la funcion escalon unitario es simplemente $1/s$ lo que es un util para analizar la respuesta de sistemas a entradas constantes.

$$u(t) = 
\begin{cases} 
0, & t < 0 \\
1, & t \geq 0
\end{cases}$$

$$\mathcal{L}\{u(t)\} = \int_0^{\infty} e^{-st} \cdot 1 \, dt = \frac{1}{s}, \quad \text{para} \, s > 0$$

## 4.funcion rampa
Nos ayuda a cconvertir una funcion que crece de forma lineal en el tiempo como $$r(t)=t$$, una expresion mas facil de manejar en el mundo de las ecuaciones y sistemas dinamicos 

$$\mathcal{L}\{r(t)\} = \mathcal{L}\{t\} = \int_0^{\infty} t e^{-st}dt$$

# TRANSFORMADA LAPLACE INVERSA
* Si las funsiones son simples, se puede usar directamente la tabla de las transformadas
 
* Si la función es una combinación o composición de varias funciones, es necesario:

- Calcular la integral de la definición de la transformada inversa.
- Usar una expansión en fracciones parciales para descomponer la función en términos más simples que se encuentren en la tabla de transformadas.

## DESCONPOSICIONEN FRACCIONES PARCIALES
La descomposición en fracciones parciales es una técnica que usamos para simplificar una fracción complicada dividiéndola en fracciones más sencillas. Esto es muy útil cuando aplicamos la Transformada Inversa de Laplace, ya que nos permite trabajar con funciones más simples que podemos buscar fácilmente en las tablas de transformadas.

## Pasos simplificados:
1. Factorizar el denominador: Se descompone el denominador en partes más simples.
2. Escribir las fracciones parciales: La fracción original se convierte en una suma de fracciones más fáciles de manejar.
3. Calcular las constantes: Se encuentran los valores de las constantes (A, B, etc.) resolviendo algunas ecuaciones.
4. Aplicar la Transformada Inversa: Finalmente, buscamos la inversa de cada fracción parcial en las tablas de transformadas.

# SISTEMAS MECANICOS 
Un sistema mecánico es básicamente un conjunto de componentes que interactúan para generar movimiento o transferir energía. Estos sistemas están presentes en muchas cosas que usamos a diario, como un auto, una bicicleta o incluso una simple puerta con bisagras. Todo sistema mecánico sigue las leyes de la física, como las de movimiento de Newton.

## Elementos principales:
Masa: Es el "peso" del objeto o cuerpo en el sistema.
Fuerza: Es lo que hace que algo se mueva o cambie su estado de reposo.
Movimiento: Describe cómo se desplaza algo, a qué velocidad y en qué dirección.
Energía: La fuerza aplicada se convierte en energía que mueve o deforma algo.
Fricción o resistencia: Es una fuerza que frena el movimiento, como cuando algo roza una superficie.
Rigidez: Mide qué tan difícil es deformar algo, como un resorte.

## Movimiento en estos sistemas:
El comportamiento de un sistema mecánico se describe con fórmulas que relacionan el movimiento, la velocidad, la fuerza y la aceleración. Un ejemplo típico es la ecuación que describe cómo se mueve una masa conectada a un resorte y un amortiguador:

$$m \ddot{x}(t) + d \dot{x}(t) + k x(t) = F(t)$$

Esto simplemente dice que el movimiento de la masa depende de su propia inercia (la masa), la resistencia (el amortiguador), y qué tan rígido es el sistema (el resorte).


# CONCLUCIONES

En conclusion la transformada de laplace es una herramienta para simplificar el analisis de sistemas lineales, ya que convierte ecuaciones diferenciales en ecuaciones algebraicas 
la transformada inversa de laplace nos permite regresar al dominio del tiempo una funcion que ha sido transformada al dominio de la frecuencia 
en los sistemas mecanicos, la aplicacion de la transformada de laplace sismplificsa el analisis de fuerzas y movimientos, convirtirndo ecuaciones extensas en problemas de facil manejo  

## REFERENCIAS

### *Ogata, K. (2010). Ingeniería de Control Moderno. Pearson Educación.*

Este libro proporciona una base sólida en la teoría de la Transformada de Laplace y su aplicación en sistemas de control.

### *Dorf, R. C., & Bishop, R. H. (2011). Sistemas de Control Moderno. Prentice Hall.*
En este texto se exploran con profundidad la Transformada Inversa de Laplace y su uso en el análisis de sistemas.
