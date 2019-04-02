# TP1

1. Selecciona bebida
2. Selecciona aditivos
3. Paga
    - (Opcionalmente) se da vuelto
4. Se dispensa la bebida
5. Se agregan aditivos

## Pago

**Todos los montos de pago son en enteros. Los dos dígitos menos significativos representan centavos.** $15.20 = 1520.

1. Obtengo el monto a pagar
2. Activo los sistemas de pago
3. Ingresa el efectivo/tarjeta
   - Se valida la tarjeta
4. Cobro
   - Doy vuelto

**expectPaymentOf**: le dice a un medio de pago el monto máximo que debe cobrar. Se dispara cada vez que se actualiza el monto ingresado.  
Por ejemplo: se espera un pago de $20.

1. expectPaymentOf(2000)
2. Ingreso 15
3. Se notifica un pago de 1500
4. expectPaymentOf(500)
5. Ingreso 10
6. Se notifica un pago de 500
7. Se devuelve vuelto de 5

Se pueden realizar pagos mixtos de efectivo y tarjeta si se paga primero parte del monto con efectivo.

**cashier:** maneja los medios de pago y acumula el monto total pagado.

## Preguntas

1. Como sería la carga de ingredientes, recetas y el manejo de precios. El caso de uso solo contempla el chequeo de stock, me limito a lo que dicen los requerimientos?
2. Precio de bebida vs precio de ingredientes  
   Asumo que cada ingrediente tiene precio y es igual para todas las máquinas.  

3. Separar las responsabilidades de stock / dispensar liquido y forzarme a usar dos mapas o juntar ambas cosas en la interfaz Dispenser?
4. Como seria la conexión con el módulo principal? Siendo realistas cada máquina le pegaría a una API HTTP del servidor que sería el módulo principal.

## Ingredientes

Los ingredientes tienen los mismos precios en todas las máquinas. El precio de una bebida esta dado por la suma de todos sus ingredientes.