---
title: Sostenibilidad y Escalabilidad
---

## Ethereum y el medio ambiente

### [PoW](https://es.wikipedia.org/wiki/Sistema_de_prueba_de_trabajo)

Proof of Work es el mecanismo de consenso que ha creado las principales blockchains (Bitcoin y Ethereum) y es lo que ha conseguido la confianza necesaria para que sean una realidad hoy.
Pero, tiene un problema, la confianza se genera a base de recursos computacionales.

El funcionamiento es sencillo:

Resolver el puzzle matemático que hace que un nuevo bloque encaje en la cadena es muy complejo y requiere muchos recursos (CPU, GPU, etc).
El primero que lo consigue lo comunica a la red y el resto comprueba que es correcto (resolverlo es difícil pero comprobarlo es muy simple) y de ahí el acuerdo (consenso) de todos los nodos en encajarlo en la cadena. El primero que lo hace se lleva una recompensa por haberlo logrado.

Bitcoin va a continuar siendo así porque se creó así. Ethereum, por el contrario, tiene un plan (desde el principio), para cambiar a un sistema más sostenible en términos ecológicos.

### [PoS](https://es.wikipedia.org/wiki/Prueba_de_participaci%C3%B3n)

Proof of Stake es un mecanismo de consenso en el que la confianza se establece en base a un depósito (Stake), de manera que si intentas engañar a la red pierdes el depósito. Así de simple y sin recursos computacionales que malgastar.

Ethereum ha completado recientemente una actualización en la que se pone en marcha una capa PoS y es el primer paso hacia un Ethereum completamente PoS (Ethereum Serenity).

Ethereum roadmap:
https://hackernoon.com/the-beginners-guide-to-ethereum-s-2020-roadmap-2ac5d2dd4881

## Escalabilidad

En realidad, en este caso, las mejoras en sostenibilidad van unidas a las de escalabilidad ya que los sistemas PoS son mucho más rápidos en términos de transacciones por segundo (TPS) ya que no hay que resolver puzzles complicados.

Sin embargo, los TPS no son lo único que importa cuando se habla de "escalabilidad" ya, por ejemplo, una red de 5TPS (como Ethereum) en la que se puedan agrupar 500 transacciones en una sola, se convierte en una red de 100TPS. Estas y otras técnicas (como la privacidad) son las que se pueden usar hoy en Ethereum.

Estas técnicas son algo tan complejo y a la vez interesante y entretenido que NO recomiendo leer nada de esto https://docs.ethhub.io/ethereum-roadmap/layer-2-scaling/zk-starks
sin antes empezar esto  https://es.wikipedia.org/wiki/Prueba_de_conocimiento_cero. Estáis avisados.

Algunas referencias más:

https://hbr.org/2018/11/making-cryptocurrency-more-environmentally-sustainable
https://digiconomist.net/ethereum-energy-consumption
