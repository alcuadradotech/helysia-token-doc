---
title: Tecnología Blockchain
---

La tecnología Blockchain surge con [Bitcoin](https://es.wikipedia.org/wiki/Historia_de_bitcoin) en 2009 y su esencia es devolver el control a los usuarios frente a un sistema totalmente centralizado.

### ¿Qué es una Blockchain?

Si se pudiera describir como "una sola cosa", sería algo así como **“un libro de cuentas distribuido”**.

Sin embargo, en general, una Blockchain **son varias cosas**, que se podrían resumir en estos cuatro conceptos:

1. Es la solución a un problema
2. Es una red pública(1) descentralizada
3. Es una base de datos inmutable
4. Es un ordenador (en el caso de [Ethereum](https://ethereum.org/), completamente programable)

Todas la Blockchains surgen, principalmente, por la necesidad de algunas personas de solucionar **el problema del intermediario financiero**. Para ello se desarrolla un **sistema descentralizado** y **distribuido** entre los ordenadores de los usuarios (o nodos), que se comporta como si fuera **un único ordenador global** y, como tal, puede ejecutar programas, los llamados **Smart Contracts**.

Además, gracias a la criptografía, **la información que se guarda en la red es inmutable**, y por tanto, totalmente confiable, aunque esto depende en gran medida del **grado de descentralización de la red**.

Las redes más confiables son las más descentralizadas. El porqué es muy simple: _quizás sea posible engañar a unos pocos ordenadores (como, por ejemplo, los de un banco o los de una red social), pero es prácticamente imposible engañar a miles de ello_.

> (1) Las Blockchains también pueden ser privadas. Esto es un simple caso de uso, en el que la red sólo es accesible para algunos usuarios. El grado de descentralización de las redes privadas es, por tanto, muy bajo. Un ejemplo cercano es la red española [Alastria](https://alastria.io/), controlada po una [lista de socios](https://alastria.io/directorio-de-socios).

### ¿Qué significa "descentralizado"?

Significa dos cosas:

1. Sin censura. Nadie puede controlar las transacciones que se ejecutan en la cadena.
2. Inmutable. Lo que se escribe una vez en la cadena, ya no se puede cambiar.

La tecnología Blockchain con un grado de descentralización adecuado, asegura la integridad y la persistencia de los datos que maneja para siempre.
Cuantos más usuarios sostengan la red, mayor grado de descentralización tiene, y por tanto, mayor confiabilidad.


### ¿Cómo funciona una Blockchain?

Debemos pensar en una Blockchain como un único ordenador global que **registra** las **transacciones** que los usuarios ejecutan en el. Las transacciones se registran en forma de paquetes que se llaman **bloques**.

Todos los bloques, desde el primero hasta el último, **están enlazados unos con otros**. Esto se consigue usando funciones criptográficas, mediante las cuales, **toda la información contenida en un bloque forma parte también del siguiente**.

De esta manera, si se quiere engañar a la cadena (ej. multiplicando mi balance por 1000), hay que cambiar la cadena entera, algo inviable, ya que todos los demás nodos poseen una copia exacta de la misma y se van a dar cuenta del engaño.

Para usar la red, **los usuarios** de la Blockchain **conectan directamente a uno de los nodos** de la red (sin intermediarios), lo que les permite insertar, directamente, transacciones en la cadena. Cuando una de estas transacciones es validada por unos cuantos nodos, ésta se inserta dentro de un bloque.

La inserción de un nuvo bloque, **tiene un coste en recursos de computación** ya que es necesario resolver un puzzle criptográfico muy complejo para asegurar la consistencia de toda la cadena. El nodo que lo consigue **obtiene una recompensa** por ello en forma de moneda nativa (Bitcoin, ETH, etc.). Esta _recompensa_ la pagan los usuarios de la red en forma de **fee** cada vez que envían una transacción para que sea insertada en un bloque.

La conexión a un nodo se hace a través de un navegador con una extensión como [MetaMask](https://metamask.io/) o una aplicación móvil como [TrustWallet](https://trustwallet.com/) (y muchas otras disponibles como "Cryptocurrency Wallets").
