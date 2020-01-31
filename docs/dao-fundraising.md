---
title: Recaudación de fondos
---

## Recaudación de fondos

Aragon Fundraising es un conjunto de aplicaciones proporciona a las organizaciones una capacidad continua de recaudación de fondos.

La aplicación permite a los usuarios comprar y canjear el token Alándalus (ALT) a través de un **creador de mercado automatizado**, que empareja automáticamente las órdenes según una **[curva de garantía](https://yos.io/2018/11/10/bonding-curves/)** ligada a la **[fórmula de Bancor](https://medium.com/@Cooperzi/bancor-formula-the-magic-of-the-maths-b339dbebe103)**. Los depósitos se almacenan en un **fondo de reserva**, que se controla por medio de un mecanismo, a modo de grifo, y se van liberando a lo largo del tiempo hacia un fondo controlado por los gestores de Al Ándalus. Esta arquitectura permite la **rendición de cuentas** entre los inversores y miembros de la gestora, a lo largo del ciclo de vida del proyecto y, al mismo tiempo, garantiza una **liquidez suficiente** para favorecer la creación de una **organización [de larga cola](https://es.wikipedia.org/wiki/Larga_cola)**.

### ¿Cómo funciona?

Los inversores pueden, en cualquier momento, comprar tokens Al Ándalus contra una cierta cantidad de garantía, como [DAI](https://makerdao.com/en/), que entra y sale del **fondo de reserva**. La emisión o el rescate de este token se ejecuta automáticamente mediante un contrato inteligente que garantiza la **liquidez absoluta** del token. Además, el precio de este token **se ajusta automáticamente** en base a su oferta a través de una **curva de garantía**.

Cada período de tiempo - por ejemplo cada mes - **se permite que una fracción del fondo de reserva fluya hacia otra cuenta**, para, de esa manera extraer fondos para financiar nuestro proyecto. La cantidad que puede ser extraída, sólo puede ser actualizada por los propios inversores, asegurando así la **responsabilidad de la organización** hacia ellos. En comparación con los métodos tradicionales de recaudación basados en acciones o tokens, no se da una suma global a los fundadores de un proyecto. En cambio, la cantidad disponible fluctúa con el tiempo. Las condiciones de inversión son transparentes e iguales para todos los participantes. Incluso los propios ingresos del proyecto pueden enviarse al fondo de reserva, para, de esa manera, aumentar el valor del token y atraer a más usuarios, que desean beneficiarse de los aumentos de precios posteriores.

#### ¿Qué es una curva de garantía?

Cuando queremos intercambiar acciones en una empresa, inmobiliaria, cooperativa, etc., tradicionalmente, hay dos formas de hacerlo: venta directa - OTC - o a través de un mercado de valores. En la OTC un comprador y un vendedor negocian un precio - o se ponen en contacto a través de un tercero - y luego realizan una transacción: este es un proceso muy lento y costoso que reduce enormemente la liquidez del activo. La venta de una casa puede, por ejemplo, llevar meses o años. Por otro lado, hay mercados basados en libros de órdenes como el mercado de valores. Éstos funcionan para activos de gran volumen como los productos básicos, donde hay muchos compradores y vendedores. Un mercado de valores con libro de órdenes empareja a compradores y vendedores cuando ambos especifican un rango de precio similar, entonces, liquidan una orden en su nombre.

**Las curvas de garantía son un novedoso mecanismo criptoeconómico que ofrece un método alternativo de fijación de precios para los activos tokenizados**. Se basan en contratos inteligentes que actúan como un creador de mercado automatizado: el contrato inteligente, emite tokens a un precio que se determina algorítmicamente mediante una fórmula determinada. Más específicamente, la recaudación de fondos de Al Ándalus se basa en la [fórmula del Protocolo de Bancor](https://about.bancor.network/protocol).


### Fórmula Bancor

En el Protocolo de Bancor, la curva de garantía mantiene un **coeficiente de reserva** constante entre la cantidad de tokens que se mantienen en el fondo de reserva y el valor total de los tokens (o capitalización del mercado). Esta relación se llama "peso del conector" o CW (siglas de connector weigh):
```
             reserva
Precio = ----------------
         suministro * CW
```
La elección del CW, moldeará la pendiente de la curva y la respuesta del precio a la oferta de tokens. Un CW cercano al 100% se aproxima a una moneda estable: el precio del token de la curva de unión es el mismo independientemente de la cantidad de garantía en el fondo común. Por el contrario, un CW bajo resulta en más recompensas para los primeros clientes pero se vuelve muy volátil después de un cierto punto de inflexión. En el caso de Aragon Fundraising el CW **se fija por defecto en un 10% para el DAI** y un 1% para el ANT. Esto se puede cambiar a través de despliegues personalizados.

![Los números y la pendiente son ilustrativos y varían según la configuración de varios parámeros](https://lh4.googleusercontent.com/ahqOfYhIIA6Sm-JN1FDe_7MXT9mlj_CGiObVzdM07UZGHshNmK0FHVGDTuGVjUnlHnUX6_sPdzdww042pLb6gt8jiycikk00ltPx9LZZYxr6Kj5G-cRReBEvL7ep8DX6f9mxA_ki)

A medida que los precios aumentan, no sólo en función de las participaciones de los inversores, sino también de los ingresos que se destinan al fondo de reserva, los inversores querrán invertir en las organizaciones que crean que van a aumentar de valor. Así, el precio de una curva de garantía representa la creencia en el valor de un proyecto, de la misma manera que el precio del valor de las acciones, representa la creencia en las ganancias presentes y futuras de una empresa.

## Componentes

La suite de aplicaciones de recaudación de fondos de Aragón se compone de cinco componentes: un fondo de reserva, una preventa, un creador de mercado, un grifo y un controlador.

### El fondo de reserva

El fondo de reserva es el contrato al que se envían los fondos utilizados para la compra de tokens de la organización. El fondo de reserva se implementa como un [Agente](https://aragon.org/agent) que permite a los inversores interactuar con contratos externos.

### Preventa

El módulo de preventa se encarga de la fase de preventa de la campaña de recaudación de fondos. Permite a las organizaciones definir un **objetivo de preventa que debe alcanzarse durante un período de tiempo determinado**, para que la campaña continua de recaudación de fondos comience realmente. Si no se alcanza este objetivo durante este período, la campaña continua no se iniciará y los inversores podrán solicitar la devolución de sus contribuciones. Si se inicia una campaña de recaudación de fondos y la preventa fracasa, es necesario volver a desplegar una nueva DAO para iniciar una nueva campaña.

A modo de mecanismo de protección, el módulo retiene los tokens de la preventa, lo que permite a los gestores asegurarse de que los tokens comprados durante la preventa no se vendan nada más abrir el mercado contínuo.

### Creador de mercado

Éste módulo proporciona liquidez a la campaña de recaudación haciendo coincidir automáticamente todas las órdenes de compra y venta de acuerdo con una curva de garantía vinculada a la fórmula Bancor. Para mitigar ataques frontales (front-running) y autorizar el trading lento (slow-trading), este módulo también agrupa todas las órdenes de compra y venta recibidas durante un período de tiempo parametrizable para que se cotejen contra un precio común.

Debido a este mecanismo de agrupación, las órdenes no se pueden pasar y devolver en una sola transacción. Primero hay que abrir una orden, esperar a que el lote actual termine y luego realizar una segunda transacción para reclamar los tokens.

### El grifo

El módulo de grifo impone un control de los fondos que se permite retirar del fondo de reserva hacia fondo discrecional. Para ofrecer más garantías a los inversores, este módulo también permite que este flujo de fondos se reduzca, asegurando así que el fondo de reserva no pueda vaciarse ni siquiera lentamente durante un largo período de tiempo.

### Controlador

El módulo controlador funciona como una API que envía todas las transacciones entrantes a uno de los módulos anteriores. Los usuarios finales sólo pueden interactuar con este contrato.

## Governanza

Para racionalizar el uso de la financiación, se implementa la plantilla de gobierno por defecto de Aragon Fundraising.

### Grupos

La plantilla de gobierno por defecto identifica dos actores: los gestores y los inversores.

#### Los gestores

Los gestores de la organización son los usuarios poseedores de tokens "de gestión" y son los que están siendo financiados por la campaña de recaudación. Éstos están representados a través de un token personalizado, el **Al Ándalus DAO Tokens** o **ALD**, y un conjunto de aplicaciones de voto dispuestas para ser utilizadas como un sistema multifirma. Sus privilegios están intencionadamente limitados para proteger a los inversores. Por lo tanto, sólo tienen los siguientes derechos:

1. **Gestionar los miembros**. El consejo decide quién debe ser incluido/excluido del consejo.

2. **Apertura de la preventa**. El consejo decide cuando debe comenzar la preventa.

3. **Gestionar los ingresos**. El consejo decide qué uso se le dará a los fondos recaudados, los cuales son periódicamente transferidos a su discreción.

4. **Apertura de votaciones**. Los gestores deciden cuándo deben abrirse nuevas votaciones para que los inversores decidan sobre el funcionamiento de la organización.

  * Crear tokens de gestión y revocar derechos de voto
  * Iniciar y ejecutar pagos desde la aplicación de Finanzas
  * Actualizar la dirección del beneficiario de los fondos que salen por el grifo.

#### Inversores

Los inversores son los que contribuyen a la campaña de recaudación, es decir, los clientes de Al Ándalis, y están representados a través del Token Al Ándalus (ALT), un token (que pueden comprar y vender a través de la interfaz de recaudación de fondos de Aragón]. **Los inversores tienen una buena parte de los derechos sobre la organización**.

**Sistema de gestión**. Los inversores deciden qué aplicaciones se instalan, cuáles se actualizan y cómo se establecen los permisos.

**Gestión de los parámetros de recaudación**. Los inversores deciden si o cómo se deben actualizar los beneficiarios, las tasas, los parámetros de colateralización y los grifos.

### Justificación

Esta arquitectura otorga una gran parte de los derechos de gobernanza a los inversores para, precísamente, proteger su inversión. Por lo tanto, es necesario mitigar las situaciones en las que un inversor que posea más del 50% de los tokens, sería el propietario de toda la organización. Por ello, los votos basados en las participaciones sólo pueden ser abiertos e iniciados por los gestores.


## Recursos

Para profundizar en el la comprensión de las DAICO, curvas y el diseño de la implementación de Aragon, recomendamos las siguientes lecturas:
​
* DAICO:
  * [Introducing Continuous Organizations](https://hackernoon.com/introducing-continuous-organizations-22ad9d1f63b7)
  * [Explanation of DAICOs](https://ethresear.ch/t/explanation-of-daicos/465) Vitalik Buterin's seminal article about DAICOs

* Bonding Curves
  * [Blockchain Spotlight - Bonding Curves: Creating liquidity and encouraging investment in new markets](http://cryptos.com/blockchain-spotlight-bonding-curves-creating-liquidity-and-encouraging-investment-in-new-markets/) Non technical introduction to bonding burves
  * [An Introduction to Bonding Curves](https://kauri.io/article/f7853f4914bd42b6bee19758a97b42ee/an-introduction-to-bonding-curves) An introduction to bonding curves

* Aragon Fundraising
  * [Introducing Aragon Fundraising](https://blog.aragon.org/introducing-aragon-fundraising/) Introduction to Aragon Fundraising
  * [Aragon Fundraising & the return of the commons](https://blog.aragon.black/aragon-fundraising-the-return-of-the-commons/) Some doors opened by Aragon Fundraising
  * [Batched Bonding Curves](https://medium.com/@billyrennekamp/batched-bonding-curves-ce69a57d8ae4) A primer on orders batching for bonding curves
