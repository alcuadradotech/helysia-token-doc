---
title: Al Ándalus DAO
---

## ¿Qué es una DAO?

Una DAO, u organización autónoma descentralizada, es una organización dirigida por reglas establecidas en contratos inteligentes y desplegados en una Blockchain en las que uno o varios tokens establen la capacidad de voto dentro de la organización.

**¿Para que sirven los votos?**

Esencialmente, para hacer efectivas las grandes decisiones, tales como asignar tokens o fondos de la organización. Si gana el "Sí", los fondos o asignaciones u otras decisiones que se incluyen en el voto, se hacen efectivas en la Blockchain, si no, simplemente no ocurre nada.

## ¿Como obtiene financiación una DAO?

Como hemos visto, las DAO disponen de varias funcionalidades, entre las más importantes, el voto. Sin embargo, hasta hace poco, no tenían una forma directa de hacer que el capital entrara y saliera de forma líquida.

### La solución de [Aragon](https://aragon.org/)

Twitter (71.4k followers) – Solidity repo (created 3/2017)

En este proyecto, utilizamos la tecnología de [Aragon](https://aragon.org/), ya que dispone del conjunto de aplicaciones la más avanzado para la creación de DAOs en la red de Ethereum, y, además, dar solución al problema de la financiación.

La solución adoptada por Aragón "Organización Continua", en la que una organización emite un token, en lo que se podría llamar, una campaña continua de recaudación de fondos, precedida por una preventa.

Las organizaciones fundadas utilizando esta solución, se caracteriza por su transparencia, responsabilidad y liquidez.

## Otras pilas de aplicaciones DAOs

### [DAOstack](https://daostack.io/)

Twitter (6.3k followers) – Solidity repo (created 9/2016)

A diferencia de Aragón, DAOstack pone mayor énfasis en resolver los problemas inherentes a la toma de decisiones descentralizada a gran escala.

En la opinión del equipo de DAOstack, las organizaciones con toma de decisiones descentralizadas, un gran número de usuarios y de propuestas, es difícil para los participantes saber qué propuestas merecen más atención, y se hace cada vez más difícil motivar a los participantes a tomarse la molestia de considerar tal cantidad de propuestas.

Técnicamente, el logro más notable de DAOstack es el mecanismo criptoeconómico de "consenso holográfico" para aproximar de manera eficiente y confiable las decisiones grupales utilizando un pequeño número de participantes. El mecanismo funciona al incentivar una red de "predictores" para hacer apuestas sobre si una propuesta pasará o no; las predicciones se usan luego (junto con otras reglas) para enfatizar las propuestas y modificar los requisitos de quórum necesarios para que la propuesta sea aprobada. De esta manera, una organización puede escalar a un número arbitrario de propuestas y de participantes sin sacrificar la velocidad o la calidad de la toma de decisiones.

En resumen: está orientada a organizaciones a gran escala.

### [Colony](https://colony.io/)

Twitter (8.3k followers) – Solidity repo (created 4/2017)

A diferencia de Aragón y DAOstack, cuyo enfoque es la gestión de una organización basada en el voto, Colony ha optado por centrarse en lo cotidiano. Con "sin permiso por defecto" como su grito de guerra, Colony se centra en gran medida en los mecanismos que, en la medida de lo posible, eliminan la necesidad de votar en las operaciones diarias.

En cuanto a la escala, en el caso de DAOstack, se logra utilizando el consenso holográfico. En el caso de Colony, la escala se logra a través de un proceso asíncrono de toma de decisiones financieras continuas (usando un árbol de dominio similar a un organigrama), lo que permite que diferentes dominios de la organización realicen sus operaciones de manera relativamente autónoma.

Técnicamente, el logro de Colony es la constelación de mecanismos que aprovechan el tiempo para permitir la asignación de recursos sin permisos. El tiempo juega un papel en Colony de dos maneras críticas: la reputación se deteriora con el tiempo (implementada a través de un proceso de extracción de reputación off-chain), y los fondos se asignan continuamente en función del tiempo (a diferencia de los métodos discretos de aprobación/rechazo). Cuanta más reputación respalde una propuesta, más rápido se financiará. La adquisición de reputación está impulsada por el trabajo en la organización (en el proyecto), lo que hace que la reputación sea portadora de información de mercado (de la misma manera que los precios).

En resumen: está orientada a la gestión de la reputación a través del trabajo.

### [Moloch](https://molochdao.com/)

Twitter (4.1k followers) – Solidity repo (created 7/2018)


A diferencia de Aragón, que lucha contra el mal gobierno, y DAOstack y Colony, que se oponen a la disfunción de la organización humana, las bases de Moloch son sólidamente racionalistas y criptoeconómicas, arraigadas, entre otras cosas, en el trauma de TheDAO.

Moloch puede describirse como un experimento de un mecanismo de coordinación, buscando crear el "proceso mínimo viable" que permita a las personas asignar recursos compartidos para conseguir un objetivo compartido, mientras minimiza agresivamente los vectores de ataque y abuso, tanto técnicos como sociales.

Técnicamente, Moloch mezcla hábilmente la computación y las capas sociales. El primero es aprovechar el tiempo y centrar la atención de los participantes en una decisión colectiva. Las propuestas se consideran en una secuencia temporizada, de manera que, los participantes malintencionados no pueden abrumar a los participantes con demasiadas decisiones. Además, las decisiones en sí mismas están limitadas de manera similar: cada propuesta incluye un crédito de cierta cantidad de tokens (el "tributo") y un débito de cierta cantidad de influencia ("derechos de voto"). Un candidato desconocido puede ofrecer un gran tributo por una pequeña influencia, mientras que un candidato conocido y respetado puede ofrecer un pequeño tributo por una gran influencia.

El segundo logro técnico fue la innovación en torno al "abandono de la ira", en el que los participantes pueden salir (con su parte de los recursos) si no están contentos con las decisiones de sus colegas. Esta innovación crea un desincentivo para la malicia e implícitamente ejerce presión social sobre los participantes para que se mantengan alineados con los objetivos de la organización.

En resumen: un sistema de toma de decisiones a través de la reputación conseguida por influencia
