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

## SISTEMA MASA RESORTE-AMORTIGUADOR

El sistema masa-resorte-amortiguador es un modelo clásico en la mecánica que describe el comportamiento de un objeto (masa) que está sujeto a la acción de un resorte y un amortiguador. Este sistema es fundamental para entender cómo las fuerzas afectan el movimiento de objetos y cómo se disipa la energía en sistemas reales

### Componentes principales:

### 1. Masa (m): 
Representa el objeto que se mueve bajo la influencia de las fuerzas del resorte y el amortiguador.

### 2. Resorte (k): 
Aplica una fuerza proporcional a la deformación del resorte, según la Ley de Hooke. Esta fuerza tiende a devolver la masa a su posición de equilibrio. La constante del resorte 
k mide la rigidez del mismo.

### 3. Amortiguador (d): 
Representa la resistencia que disipa energía, como la fricción o un amortiguador real. Su función es reducir la velocidad del sistema con el tiempo. La fuerza de amortiguamiento es proporcional a la velocidad de la masa.

### 4. Fuerza externa (F(t)): 
Es cualquier fuerza que se aplique desde el exterior, como una fuerza constante o periódica.

## Ecuación del movimiento:
El comportamiento del sistema está descrito por la siguiente ecuación diferencial de segundo orden:
$\[m \ddot{x}(t) + d \dot{x}(t) + k x(t) = F(t)\]$

## Tipos de respuesta del sistema:
Dependiendo de los valores de d, el sistema puede tener diferentes comportamientos:

### 1. Subamortiguado: 
Si la resistencia es baja, la masa oscila alrededor de la posición de equilibrio, pero eventualmente se detiene.
### 2. Criticamente amortiguado: 
La resistencia es tal que el sistema regresa a la posición de equilibrio lo más rápido posible sin oscilar.
### 3. Sobreamortiguado: 
Si la resistencia es muy alta, el sistema vuelve lentamente a la posición de equilibrio sin oscilar.

## SISTEMAS ACOPLADOS 
Los sistemas acoplados son aquellos en los que dos o más sistemas interactúan entre sí, influyendo mutuamente en su comportamiento. Estos sistemas están conectados de tal forma que el movimiento o la dinámica de un sistema afecta directamente al otro, lo que genera una relación interdependiente.

### Características de los sistemas acoplados:

### 1. Interacción: 
Los sistemas no son independientes; las variables que describen uno de los sistemas influyen en las variables del otro.

### 2. Ecuaciones interrelacionadas: 
Las ecuaciones que describen cada sistema están vinculadas. Es decir, las ecuaciones diferenciales o algebraicas de un sistema contienen términos que dependen de las variables del otro sistema.

### 3. Transferencia de energía: 
Existe una transferencia de energía, fuerza o información entre los sistemas. Esto puede ser a través de fuerzas físicas (como una conexión elástica o un amortiguador) o señales eléctricas o de otro tipo.

## Ecuaciones en sistemas acoplados:
Las ecuaciones diferenciales que describen estos sistemas suelen ser de la forma:

$\[m_1 \ddot{x}_1 + d_1 \dot{x}_1 + k_1 x_1 - k_2 (x_2 - x_1) = F_1(t)\]$

$\[m_2 \ddot{x}_2 + d_2 \dot{x}_2 + k_2 (x_2 - x_1) = F_2(t)\]$

Aquí, x 1​ y x 2 representan el desplazamiento de cada masa, k 2 es la constante del resorte que conecta las dos masas, y F1(t) y 𝐹2(t) son las fuerzas externas aplicadas a cada masa. Las ecuaciones están interrelacionadas porque el movimiento de una masa afecta directamente a la otra.


# CONCLUCIONES

En conclusion la transformada de laplace es una herramienta para simplificar el analisis de sistemas lineales, ya que convierte ecuaciones diferenciales en ecuaciones algebraicas 
la transformada inversa de laplace nos permite regresar al dominio del tiempo una funcion que ha sido transformada al dominio de la frecuencia 
en los sistemas mecanicos, la aplicacion de la transformada de laplace sismplificsa el analisis de fuerzas y movimientos, convirtirndo ecuaciones extensas en problemas de facil manejo

Al estudiar los sistemas acoplados y el sistema masa-resorte-amortiguador, me ha quedado claro cómo las pequeñas conexiones entre diferentes partes de un sistema pueden afectar enormemente su comportamiento global. Es interesante ver cómo algo tan cotidiano como un resorte o un amortiguador puede cambiar completamente la forma en que un objeto se mueve o responde a fuerzas externas.  

## REFERENCIAS

### *Ogata, K. (2010). Ingeniería de Control Moderno. Pearson Educación.*

Este libro proporciona una base sólida en la teoría de la Transformada de Laplace y su aplicación en sistemas de control.

### *Dorf, R. C., & Bishop, R. H. (2011). Sistemas de Control Moderno. Prentice Hall.*
En este texto se exploran con profundidad la Transformada Inversa de Laplace y su uso en el análisis de sistemas.
