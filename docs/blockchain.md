---
title: La Tecnología Blockchain
---

La tecnología Blockchain surge con [Bitcoin](https://es.wikipedia.org/wiki/Historia_de_bitcoin) en 2009 y su esencia es devolver el control a los usuarios frente a un sistema totalmente centralizado.

## ¿Qué es una Blockchain?

Si se pudiera describir como "una sola cosa", sería algo así como **“un libro de cuentas distribuido”**.

Sin embargo, en general, una Blockchain **son varias cosas**, que se podrían resumir en estos cuatro conceptos:

1. Es la solución a un problema
2. Es una red pública¹ descentralizada
3. Es una base de datos inmutable
4. Es un ordenador (en el caso de [Ethereum](https://ethereum.org/), completamente programable)

Todas la Blockchains surgen, principalmente, por la necesidad de algunas personas de solucionar **el problema del intermediario financiero**. Para ello se desarrolla un **sistema descentralizado** y **distribuido** entre los ordenadores de los usuarios (o nodos), que se comporta como si fuera **un único ordenador global** y, como tal, puede ejecutar programas, los llamados **Smart Contracts**.

Además, gracias a la criptografía, **la información que se guarda en la red es inmutable**, y por tanto, totalmente confiable, aunque esto depende en gran medida del **grado de descentralización de la red**.

Las redes más confiables son las más descentralizadas. El porqué es muy simple: _quizás sea posible engañar a unos pocos ordenadores (como, por ejemplo, los de un banco o los de una red social), pero es prácticamente imposible engañar a miles de ello_.

> ¹ Las Blockchains también pueden ser privadas. Es un simple caso de uso, en el que la red sólo es accesible para algunos usuarios. El grado de descentralización de las redes privadas es, por tanto, muy bajo. Un ejemplo cercano es la red española [Alastria](https://alastria.io/), controlada por una [lista de socios](https://alastria.io/directorio-de-socios).

## ¿Cuántas blockchains existen?

Existen muchas y de muy diversos tipos:

* En la Wikipedia se pueden visualizar según año de lanzamiento y características: [List of cryptocurrencies](https://en.wikipedia.org/wiki/List_of_cryptocurrencies)
* En CoinMarketCap, según la capitalización de mercado: [CoinMarketCap](https://coinmarketcap.com/)

## ¿Qué significa "descentralizado"?

Significa dos cosas:

1. Sin censura. Nadie puede controlar las transacciones que se ejecutan en la cadena.
2. Inmutable. Lo que se escribe una vez en la cadena, ya no se puede cambiar.

La tecnología Blockchain con un grado de descentralización adecuado, asegura la integridad y la persistencia de los datos que maneja para siempre.
Cuantos más usuarios sostengan la red, mayor grado de descentralización tiene, y por tanto, mayor confiabilidad.

En este enlace se pueden visualizar los [nodos de la red Ethereum](https://ethernodes.org/countries) según su ubicación, y en este, [los nodos de Bitcoin](https://bitnodes.io/).


## ¿Cómo funciona una Blockchain?

Debemos pensar en una Blockchain como un único ordenador global que **registra** las **transacciones** que los usuarios ejecutan en el. Las transacciones se registran en forma de paquetes que se llaman **bloques**.

> #### **Practica:**
> Examina las transacciones que contiene un bloque de la cadena ethereum. Por ejemplo, el bloque [5000000](https://etherscan.io/block/5000000) contiene [109 transacciones](https://etherscan.io/txs?block=5000000).
> Un bloque interesante es el bloque [0](https://etherscan.io/block/0), que contiene 8893 transacciones y es el que origina la cadena Ethereum en 2015. De ahí el nombre que se le da al primer bloque de una blockchain: el GENESIS.

Todos los bloques, desde el primero hasta el último, **están enlazados unos con otros**. Esto se consigue usando funciones criptográficas, mediante las cuales, **toda la información contenida en un bloque forma parte también del siguiente**.

![Cadena de bloques](https://docs.google.com/drawings/u/0/d/1rGQthLcURJx2bMn08AQambX2SftvE4gbdadtRv5q6_8/export/jpeg?id=1rGQthLcURJx2bMn08AQambX2SftvE4gbdadtRv5q6_8&pageid=p)

#### ¿Qué pasa si queremos engañar a la cadena?

Si se quiere engañar a la cadena (por ejemplo, multiplicando mi balance por 1000), hay que cambiar la cadena entera, ya que cada bloque, contiene la información del anterior, y por tanto si se quiere cambiar uno, hay que cambiarlos todos. Algo inviable, ya que todos los demás nodos poseen una copia exacta de la misma y se van a dar cuenta del engaño.

#### ¿Qué es un Hash?

Un hash **es el resultado de una función** aplicada a una entrada (normalmente cadenas de texto) que _resume_ esta entrada. Éste resumen, contiene la misma información que la entrada, pero en un formato mucho más comprimido y de longitud fija.

En este diagrama de la Wikipedia, se puede ver cómo funciona:

![Función hash](https://upload.wikimedia.org/wikipedia/commons/thumb/1/1c/Hash_function2-es.svg/320px-Hash_function2-es.svg.png)

> #### **Practica:**
> Prueba a usar la [función hash](http://emn178.github.io/online-tools/keccak_256.html) que utiliza Ethereum.

## ¿Cómo se usa la red?

Para usar la red, **los usuarios** de la Blockchain **conectan directamente a uno de los nodos** de la red (sin intermediarios), lo que les permite insertar, directamente, transacciones en la cadena. Cuando una de estas transacciones es validada por unos cuantos nodos, ésta se inserta dentro de un bloque y forma parte de la cadena.

La inserción de un nuevo bloque **tiene un coste en recursos de computación**, ya que es necesario resolver un puzzle criptográfico muy complejo para asegurar la consistencia de toda la cadena. El nodo que lo consigue **obtiene una recompensa** por ello en forma de moneda nativa (Bitcoin, ETH, etc.). Esta _recompensa_ la pagan los usuarios de la red en forma de **fee** cada vez que envían una transacción para que sea insertada en un bloque.

La conexión a un nodo a nivel de usuario, se hace a través de un navegador con una extensión como [MetaMask](https://metamask.io/) o una aplicación móvil como [TrustWallet](https://trustwallet.com/) (y muchas otras disponibles como "Cryptocurrency Wallets"). Aprenderemos cómo funcionan en la sección [Wallets](/alandalus-token-doc/docs/wallets)
