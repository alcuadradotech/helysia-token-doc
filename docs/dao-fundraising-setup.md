---
title: Configuración de la DAO Helysia
---

## Crear una DAO

## Configurar la preventa

La plantilla pr defecto de Aragon Fundraising permite configurar una campaña de preventa con las siguientes características:

1. Garantiza una reserva mínima y un tope de fondos retirables
2. Ofrece transparencia e igualdad de oportunidades a los inversores
3. Automatiza la inicialización de la curva testeando la métrica de la campaña contra sus valores mínimos

### Configuración de la preventa

  * **Objetivo**: La cantidad de DAI que la campaña de preventa debe recoger para que la curva se inicialice.
  * **Precio**: Este es el precio al que los clientes que participan en la preventa comprarán los tokens. Esto asegura la igualdad de condiciones al ofrecer el mismo precio a todos los participantes en la fase de preventa. Este precio se calcula automáticamente de acuerdo con los términos comerciales que se detallan a continuación.
  * **Período**: Cuánto tiempo dura la campaña de preventa. Si el objetivo no se alcanza, los fondos se reembolsan a los participantes. Si el objetivo se alcanza antes de este límite, la preventa se cierra y la curva puede ser iniciada.
  * **Tokens ofrecidos**: El porcentaje de la oferta inicial tokens que se ofrecerá durante la preventa. El resto de este suministro se acuñará y se enviará a la DAO si la preventa tiene éxito.
  * **Fondos retirables**: El porcentaje del objetivo de la preventa que se enviará a la DAO si la preventa tiene éxito. El resto de los fondos aportados se enviarán al fondo de reserva apoyar el mercado.

#### Condiciones de devengo

  * **Cliff**: Tiempo en días, a partir del cual empiezan a ser adjudicados parcialmente los tokens a los inversores de preventa.
  * **Calendario de devengos**: Tiempo en días, a partir del cual se entrga el total de los tokens a los inversores. Para evitar el trading inmediato, el total de los tokens que se compran en la preventa sólo pueden devengarse a partir de un tiempo determinado.

### Adquisición de tokens en la preventa

1. El usuario participa con la cantidad deseada(1), lo que requiere la firma de **2 transacciones**(2).

> (1) O la que se le ofrezca en la conformación de la transacción, es decir, se puede establecer una cantidad fija en las interfaces externas desarrolladas para la preventa. No obstante, si se publicita la URL de la organización, los usuarios siempre podrán adquirir la cantidad que deseen.

> (2) Técnicamente, la primera consiste en dar permiso (Approve) al contrato de la Stable Coin (DAI) para que el contrato de preventa, pueda utilizar el DAI del usuario, y la segunda consiste en gastar el DAI aprobado en la anterior, en el cotrato de preventa (Contribute).

### Muy importante desde el punto de vista de los usuarios - (1) Preventa!!!

Los inversores **no pueden ni vender ni transferir** los tokens adquiridos durante la preventa hasta que se cumplan las condiciones de devengo.

### Condiciones del mercado posterior a la preventa

  * **Precio inicial del token**: El precio inicial en el momento de la puesta en marcha del mercado.
  * **Crecimiento esperado**: Con la finalidad de ralizar los cálculos oportunos, se debe especificar una capitalización máxima de mercado. Cuando se alcanza este límite, se puede operar en el mercado, pero el precio ya no sube más. Debe ser un múltiplo de la capitalización de mercado inicial y, a todos los efectos, se puede configurar como un número irrealmente alto, para crear un extremo superior de la curva útil totalmente plano.

### Muy importante desde el punto de vista de los usuarios - (2) Mercado!!!

Los usuarios que compran tokens en el mercado abierto, **pueden vender y transferir** los tokens adquiridos sin restricciones, mientras que los que los adquirieron en preventa, no pueden hacerlo, al menos hasta que se cumpla el periodo de Cliff.

#### Configuración avanzada

  * **Longitud de lote**: se puede usar para establecer cuántos bloques de Ethereum dura un lote. Un lote contiene varias ódenes de conpra/venta.
  * **Deslizamiento de DAI**: Es una medida de protección mediante la cual, si el precio del lote difiere en un porcentaje más alto que esta métrica, las órdenes se cancelan y los fondos se devuelven a los usuarios.
  * **Deslizamiento de ANT**: la misma protección para el ANT.

  * **Asignación mensual inicial**: Es la cantidad de fondos que se envían al grifo cada mes. El grifo se puede abrir las veces que se desee durante el mes, pero sólo saldrá, como máximo esta cantidad.

  * **Límite inicial del grifo**: Es la cantidad mínima de fondos de reserva a partir de la cual, el grifo se congela hasta que la reseva vuelva a contar con fondos suficientes. Con esto se consigue evitar que la curva vaya cero o negativo, proporciona cierta estabilidad de precios y genera la necesaria percepción de responsabilidad fente a los inversores.


#### Adquisición de tokens en el mercado

1. El usuario crea una orden de compra (esto, al igual que en la preventa, requiere la firma de **2 transacciones**).
2. El mercado recibe la orden y la incluye en un lote. Cuaando se cumple la condición de "longitud de lote", se ejecutan las ordenes del lote
3. Una vez ejecutadas, el usuario puede "reclamar" en cualquier momento los tokens
