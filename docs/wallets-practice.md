---
title: Practicar con MetaMask
---

Con MetaMask podemos usar la red de pruebas Rinkeby para hacer nuestras primeras transacciones y familiarizarnos con todo el ecosistema Ethereum sin necesidad de utilizar Ether _de verdad_.

## Seleccionar la red de pruebas

> En esta sección no utilizaremos dinero de verdad

Debemos seleccionar la red de pruebas **Rinkeby**.

![Rinkeby en MetaMask](https://doc-0g-1s-docs.googleusercontent.com/docs/securesc/o87etst956u3s6b30klg4k1j8c225e6i/gum3n808tqpg2lhto7ak1gk7a1d4dil2/1582534800000/03990475819448209732/03990475819448209732/1l4SLS4oygss67BmperFun9ApXy6k90QM?e=download&authuser=0)

## Crear un par de cuentas

Vamos a crear un par de cuentas cuenta para poder hacer pruebas.

Haremos click en **"+ Crear cuenta"**, le asignaremos un **alias**, por ejemplo _Rinkeby 1_. Repetimos el proceso para crear la cuenta _Rinkeby 2_.

## Conseguir un poco Ether (_de mentira_)

Para utilizar la red Ethereum necesitamos Ether. En la **red principal**, necesitaríamos comprar algo (o minarlo), para poder hacer transacciones, ya que, como sabemos, cada una nos va a costar un pequeño _fee_.

En la **red de pruebas Rinkeby**, podemos conseguir un poco de Ether _de mentira_ en un grifo (en inglés _faucet_) si tenemos [Facebook](https://faucet.rinkeby.io/) o [Twitter](https://twitter.com/).

Los pasos son los siguientes:

1. Copiar la dirección de la cuenta _Rinkeby 1_

![Copiar la cuenta 1](https://doc-10-1s-docs.googleusercontent.com/docs/securesc/o87etst956u3s6b30klg4k1j8c225e6i/5hbc65k694m905hadoomldnagbalsi51/1582527600000/03990475819448209732/03990475819448209732/1V8nEIeG9Y45tVmhsMUmi3bgoKt6n9CV_?e=download&authuser=0&nonce=s5mnsv1odsim4)

2. Escribimos un tuit o una publicación en Facebook, cuyo contenido sea la dirección de la cuenta _Rinkeby 1_ (pegamos la dirección)

3. Copiamos el enlace a esa publicación o tuit (como por ejemplo esta https://twitter.com/vicnala/status/1231691651640414208)

4. Nos dirigimos a la página [faucet.rinkeby.io](https://faucet.rinkeby.io/) y pegamos el enlace en el cuadro de texto y solicitamos 3 Ethers.

5. Pasamos por el Captcha, y listo.

Sólo tenemos que esperar unos segundos y comprobar nuestro balance en MetaMask!.


## Mi primera transacción

Bien. Estamos listos para hacer nuestra primera transacción! Es muy sencillo:

1. Cambiar a la cuenta _Rinkeby 2_ haciendo click en el **círculo de colores** y copiar la dirección
2. Cambiar a la cuenta _Rinkeby 1_ y presionar el botón **Enviar**
3. Pegar la dirección de la cuenta _Rinkeby 2_ en el cuadro **Añadir destinatario**
4. Escribir `1` en el cuadro **Cantidad** y hacer click en el botón **Siguiente**
5. Revisar los datos de la transacción, en concreto, en el coste de la misma o _fee_ y hacer click en **Confirmar**

Y listo. En unos segundos tendrás confirmada la transacción en la blockchain.

Vamos a detenernos un poco aquí a revisar todos los detalles de lo que acaba de ocurrir:

#### Balances

1. El balance de la cuenta _Rinkeby 1_ ha disminuido en 1 ETH
2. El balance de la cuenta _Rinkeby 2_ ha aumentado en 1 ETH

#### Detalles

Como es obvio (esto es una blockchain) la transacción se ha registrado en un bloque y se ha publicado en la cadena. Vamos a verlo:

Si hacemos click en nuestra transacción, se despliega y vemos un montón de detalles:

![Ver en Etherscan](https://doc-0k-1s-docs.googleusercontent.com/docs/securesc/o87etst956u3s6b30klg4k1j8c225e6i/sd26j7dgab58p9mmu5aspn66l62np379/1582533900000/03990475819448209732/03990475819448209732/1XxB7OG7Tu59TDecJysUyReGHmxQFgmIx?e=download&authuser=0&nonce=7llri0bqukros&user=03990475819448209732&hash=4cg4q34tmuut0i8nvpe9nokokg9e77rg)

Sin embargo, **si necesitamos ver todos los detalles** de una transacción, deberemos hacer click en el botón **↗** (Ver en Etherscan).

**Etherscan** es un explorador de la blockchain Ethereum y es el sitio dónde **debemos consultar y revisar nuestras transacciones**.

> El sitio que vemos es **[rinkeby.etherscan.io](https://rinkeby.etherscan.io)** y corresponde a la red de pruebas **Rinkeby**. El sitio de **la red principal de Ethereum** es **[etherscan.io](https://etherscan.io)** y ahí, las cosas, **son de verdad**.

## Importar una cuenta

En la sección cuentas vimos que la **clave privada** contiene, a su vez, la parte pública. Vamos a comprobarlo: prueba a importar la clave privada del ejemplo de la sección [Cuentas](/alandalus-token-doc/docs/ethereum-accounts) en MetaMask y comprueba que la clave pública coincide. (para importarla debemos hacer click en el **círculo de colores** y después en **Importar cuenta**).

> El detalle final es que **todo el mundo que haya importado esa cuenta es dueño de todos los activos de esa cuenta**, así que, el primeo que llega, la puede vaciar sin contemplaciones porque, de hecho, es suya. De aquí **la importancia de guardar en lugar seguro las claves privadas**. 
