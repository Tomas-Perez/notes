# Sistemas distribuidos

Definicion: conexion independiente de computadoras que se le presenta al usuario como un sistema coherentes.

Cloud computing: en el libro de tanenbaum al conectar una red al internet, la representaba en el diagrama como una nube.

**Escalabilidad**
La capacidad de crecer. Tenemos una capacidad y en el caso que sea necesario podemos aumentarla. A diferencia de un sistema que utilice muchas computadoras pero no puede agregar más.

**Disponibilidad**
Una aplicacion deberia estar disponible todo el tiempo. Una falla o la saturacion de una computadora puede afectar mi disponibilidad.

**Compartir recursos**
CPU, memoria, redes. Si no tengo capacidad en una computadora puedo utilizar la de otra que no esta ocupada.

**Performance**
El sistema se satura de tal manera que se degrada la performance. Si llega al momento de saturarse el sistema, el tiempo disponible para aumentar la capacidad durante ese problema es 0. Necesito una manera de aumentar la capacidad instantaneamente.

**Reducir costos**
Podemos ajustar nuestra capacidad on demand. Aunque comprar una computadora puede salir mas barato que contratar lo mismo en amazon, si deseo soportar los picos de carga que espero tener, voy a necesitar comprar muchas mas computadoras que lo que voy a usar en todo momento.

## Escalabilidad

### Tamaño

Recursos

- Vertical: aumentar la capacidad de la misma máquina
- Horizontal: agregas más máquinas

Usuarios

### Geograficamente

Poder crecer a nivel geografico a través del planeta. Si me expando a otros continentes voy a querer agregar máquinas mas cercanas a los clientes. Voy a necesitar una base de datos global distribuida para poder acceder a los datos desde cualquier lugar.

### Administración

Administrar todos los recursos de manera automatica. Cloud computing transformo un problema de hardware en un problema de software. Da la capacidad de manejar la infraestructura con código.

### Tecnicas de escalabilidad

**Particionar**
Por mas que replique todos los datos, si en algun momento se llena una maquina no tengo manera de continuar creciendo. Tengo que dividir los datos.

## Disponibilidad

Lograr sistemas a los que no les afecte las fallas. Las fallas siempre van a estar, pero tienen que ser transparentes al usuario, que no las vea.
Como manejar las fallas:

- Detección: chequear que los datos sean correctos antes de que los vea el usuario. Guardo cada dato con su hash y me aseguro que coincidan.
- Enmascarado: retransmisión de los mensajes
- Tolerar los errores: no puedo evitar que ocurran, pero puedo tolerarlos. Cuando se cae una máquina, levanto otra tomando los datos que estan replicados en el resto.
- Recuperación: logear las transacciones que se hicieron a disco para poder rehacerlas.

## Google vs Amazon

Los sistemas distribuidos de google se basan en la orquestración. Un director dirije el resto de los componentes.

En cambio Amazon, utiliza "coreografia", donde cada componente reacciona a lo que realiza el otro.

## Grids vs Clusters

|          Grids           |      Clusters      |
| :----------------------: | :----------------: |
| Multiples organizaciones | Misma organizacion |
|       Heterogeneo        |     Homogeneo      |

---
