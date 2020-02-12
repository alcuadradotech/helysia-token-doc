---
title: Tokens
---

## ¿Qué es un Token?

**Conceptualmente**, un token es la representación digital de un valor. En términos generales: **es una moneda digital**.

En el **ámbito empresarial** sería una unidad de valor que una organización crea para auto-gobernar su modelo de negocio y dar la capacidad a sus usuarios de interactuar con sus productos, a la vez que facilita la distribución de beneficios a todas las partes interesadas.

**Técnicamente**, es un programa, también llamado "Smart Contract", que se ejecuta en una Blockchain y que cuenta con funciones que definen su comportamiento.

**Bitcoin** o **Ethereum** son algunos de los Tokens más conocidos y usados. En estos casos, el valor que representan es un valor monetario y por ello, generalmente se llaman Criptomonedas. En este caso, son, además, el propio soporte de la red que se usa para generarlos, ya que son **el incentivo** que obtienen aquellas personas que deciden participar en el mantenimiento de estas redes.

El proceso de insertar bloques en la cadena se llama **minado** en el caso de Bitcoin y la actual Ethereum y, **validación** o **consenso** en el caso de Blockchains como Stellar, EOS o Tron.

### El Token ERC-20

Desde que la Blockchain Ethereum se lanzó en 2015 ya no es necesario desplegar una red propia para generar un Token (como en Bitcoin o la propia Ethereum), ya que Ethereum es una plataforma programable en la que se pueden crear aplicaciones. Desde entonces, cualquier usuario puede crear sus propios Tokens (en realidad, cualquier tipo de aplicación) usando la red de Ethereum como soporte.

El **ERC-20** es el estándar más utilizado en la industria de las criptomonedas y define las funciones básicas que debe implementar el Token (recordamos que se trata de un programa) para que pueda interactuar de forma estándar con el resto de Tokens desplegados en la red, con otras plataformas como los exchanges e incluso con otras Blockchains.

Estas funciones son las siguientes:

* **Name** (opcional) – Nombre del Token.
* **Symbol** (opcional) – Símbolo del Token.
* **Decimals** (opcional) – El número de decimales que utiliza el Token.
* **TotalSupply** – Suministro total de Tokens que existirán.
* **BalanceOf** – Saldo de la cuenta del propietario.
* **Transfer** – Transferencia a…
* **TransferFrom** – Transferencia desde… (interfaz con exchanges)
* **Approve** – Permite la retirada de fondos.
* **Allowance** – Devuelve la cantidad que se puede retirar.

Además, se define la emisión de ciertos eventos;

* **Transfer** – Activado cuando se transfieren los Tokens.
* **Approval** – Activado siempre que se aprueba la transferencia.

### Tipos de Tokens en función de su utilidad

Aunque muchos Tokens siguen el estándar ERC-20, desde el punto de vista legal y de utilidad, pueden ser muy diferentes en función de cómo se defina la propia utilidad.

#### Payment Tokens o criptomonedas

Son un medio de intercambio de valor. Los ejemplos más conocidos son Bitcoin y Ether.

#### Utility Tokens

Tokens que pueden ser canjeados por activos o servicios de la propia entidad que los emite. Por ejemplo, si el emisor del Token es una empresa que lanza una plataforma descentralizada de coches compartidos, cada kilómetro de viaje podría estar representado con un Token.
Los Tokens son una forma de intercambiar valor entre los participantes de la red al representar **unidades de servicio**. Como tales, se denominan Utility Tokens.

#### Security Tokens

Son instrumentos de inversión.

Tokens que representan activos, como capital, deuda/préstamos o fondos de inversión. En muchos sentidos y en la mayoría de las regulaciones, estos Tokens deben considerarse equivalentes a los valores en el mundo financiero.

Los Security Tokens (o Tokens de inversión) son activos que representan una expectativa de (y un derecho sobre) los flujos de caja futuros resultante de la actividad del emisor.

Los Security Tokens están regulados y, en la mayoría de los casos, respaldados por activos subyacentes. Por tanto, pueden producir un rendimiento regular para sus titulares, al tiempo que proporcionan más estabilidad y garantías para los inversores.

Dado que el propósito principal del Token es generar un aumento de valor monetario para su titular, será considerado, legalmente, como un valor. Y por tanto, será más complicado venderlo al público en general por los requisitos legales que conlleva hacerlo.

En Europa, algunas de las leyes que se aplican son: **Prospectus Directive**, **MiFid**, **AIFMD** y **UCITS**. Por tanto, hay varias cosas que hay que tener en cuenta a la hora de emitir este tipo de tokens:

* **AML/KYC**: suele ser necesario verificar la identidad de los inversores.
* **Prior authorization**: suele ser necesario notificar previamente a los reguladores.
* **Eligibility**: suele ser necesario establecer normas de admisión (no todo el mundo puede comprar estos tokens).

### Otros tipos de Tokens en función de su diseño

Además de estándar ERC-20, existen muchos otros que se tienen distintas utilidades. Algunos ejemplos son:

* **ERC-721**: non-fungible Tokens (NFTs), por ejemplo [CryptoKitties](https://www.cryptokitties.co/)
* **ERC-1155**: Una interfaz que permite manejar distintos tipos (ej. ERC-20 y ERC721)
* Y [muchos más](https://eips.ethereum.org/erc) definidos en las EIPS de Ethereum
