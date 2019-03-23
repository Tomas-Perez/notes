# Casos de uso

## Relaciones

**Include:** un caso de uso puede incorporar el comportamiento de otros casos de uso como fragmentos de su propio comportamiento.  
La relación de include apunta al caso de uso a ser incluido.

**Extend:** se puede insertar comportamiento adicional en un CU base que no tiene conocimiento sobre él.  
La relacion de extend señala el CU que se extenderá.

**Generalización:** un CU se puede especializar en uno o más hijos.  
Cualquier CU hijo se puede utilizar en una situación en la cual se espera el CU padre.  
Generalización es un mecanismo de herencia.

## Template

MCU: Modelo Caso de Uso

**CU {nro / 001}:** Nombre (MCU_nro_nombre)

**Version:** Cada vez que se actualiza el caso de uso, aumento la version.

**Referencias:** Casos de uso que incluyo, excluyo, etc. También se incluiría referencias a los requerimientos

**Precondición:** aquello que tiene que ejecutarse antes que se ejecute el CU.

**Postcondición:** aquello que sucede despues de ejecutar el CU.

**Secuencia alternativa:** alternativa o de excepcion

- Alternativo: es un camino que es exitoso, pero no es el más usado.
- Excepción: captura un camino de problema. Una excepción es una condición de error que es lo suficientemente importante para que la aplicación lo capture.
