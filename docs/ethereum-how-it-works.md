---
title: ¿Cómo funciona?
---

Como cualquier otra blockchain, Ethereum almacena transacciones en bloques.

Entonces, ¿qué la hace diferente de otras blockchains como, por ejemplo Bitcoin?. - **Que es programable**.

## ¿Programable?

Y, ¿Cómo se programa?

Muy sencillo. Escribes un [programa](https://solidity.readthedocs.io/en/v0.5.11/introduction-to-smart-contracts.html#storage-example), lo almacenas en la blockchain (usando transacciones) y la **Máquina Virtual de Ethereum** los ejecuta. En resumen, Ethereum es un ordenador global programable que ejecuta tus programas y almacena los resultados en un libro de cuentas público y global.

Estos programas se suelen llamar **Smart Contracts**, pero no som más que _programas_.

## Transacciones

Lo primero que piensas cuando escuchas la palabra **transacción** es en una transacción monetária. En Ethereum, esto es así, pero además el concepto **transacción** se amplía de manera que se puede utilizar para cualquier cosa (entre otras, _transferir_ Ether o cualquier otro token de una cuanta a otra).

En este [programa](https://solidity.readthedocs.io/en/v0.5.11/introduction-to-smart-contracts.html#storage-example), por ejemplo, una transacción que llame a la función _set_, con el valor 100, almacena el valor 100 en la blockchain. Así de sencillo y revolucionario a la vez.

Otro ejemplo es el propio Ether (o cualquier otro token). En este caso, el programa tiene definida una función que se llama [transfer](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-20.md#transfer). Una transacción que llame a la función _transfer_, con la cuenta de tu amigo y el valor 100 como parámetros, envía 100 Ethers a tu amigo. De nuevo, así de sencillo y revolucionario a la vez.

> #### **Practica:**
> Analiza los campos que contiene una transacción en Ethereum, por ejemplo, [esta transacción](https://etherscan.io/tx/0x0b5428355681ce7754646ae6b9989cc17f6828f786435bbfd558798793b45dd8). No olvides hacer click en "Click to see More" para ver la información completa de la transacción. Hay campos muy interesantes como el coste (fee) de la transacción y, por supuesto el valor transferido.
