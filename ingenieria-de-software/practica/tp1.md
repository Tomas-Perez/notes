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