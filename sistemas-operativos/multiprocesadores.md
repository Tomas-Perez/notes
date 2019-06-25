# Multiprocesadores (unidad 8)

Unidades 6 y 7 no entran al final
8.2.4 No va
8.2.7 No algoritmos, solo introduccion (alg det de grafos, alg eu iniciado por emisor / receptor)
8.3.6 No va
8.3.7 No va
8.3.9 No va
8.4.5 No va
8.5 No va
8.6 No va

- Multiprocesadores
- Multicomputadoras
- Sistemas distribuidos

## Multiprocesadores

Memoria compartida sin memoria cache: unico bus  

Con memoria cache, unico bus  

Memoria privada en cada CPU, cada CPU tiene un bus a su memoria privada y un bus a la memoria compartida.

### Acceso a memoria

#### UMA

Unified memory access. El acceso a memoria es igual para todos los procesadores.

##### NC-NUMA

(No cache?) NUMA.

##### CC-NUMA

Cache coherent NUMA.

#### NUMA

Non unified memory access. Se establecen prioridades para diferenciar las velocidades.

### Conexiones a memoria

#### Barras cruzadas

Tantos modulos de memoria como CPUs. Cada CPU se interconecta con todos los modulos de memoria.

Cuando una CPU quiere utilizar una memoria bloquea el acceso a esa memoria en particular, no a todas. Dos CPU no pueden utilizar el mismo modulo al mismo tiempo, pero todas las CPU pueden acceder a un modulo al mismo tiempo.

En cada cruce de conexion hay un interruptor al activarse, conecta a un CPU a un modulo de memoria y evita que los demás se conecten.

#### Multi-etapas

CPU 111 a Módulo 101.

Tomamos cada bit del modulo de izquierda a derecha. Cada bit me dice que salida tomar de la etapa. 0 es la salida superior, 1 es la salida inferior.

De Módulo a CPU se repite el mismo procedimiento, pero se leen los bits del CPU, de derecha a izquierda.

Es bloqueante ya que si dos CPUs quieren routear por una etapa al mismo tiempo, uno tiene que esperar que el otro se routee. Despues, una vez que el primer CPU routee el otro puede continuar *por otro camino*.

### Distribucion del SO

#### Maestro - esclavo

Un solo CPU se ocupa de ejecutar el sistema operativo.

#### Simétrica

Cada CPU puede ejecutar la porcion del sistema operativo.

### Algoritmos de distribucion de los procesos en las CPU

#### Tiempo compartido

## Multicomputadoras

Distintas computadoras, con sus recursos independientes. Tienen conexiones especiales dedicadas entre sí.

## Sistemas distribuidos

Distintas computadoras, conectadas por red, ya sea LAN, WAN, etc.
