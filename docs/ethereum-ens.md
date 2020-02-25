---
title: Ethereum Name Service
---

> El ENS **es un servicio de pago**. Cada registro cuesta $5 al año

El servicio de nombres de Ethereum [ENS](https://ens.domains/) resuelve un problema fundamental que existe con las cuentas:

**Las cuentas de usuario son imposibles de memorizar**

## ¿Qué es el ENS?

El ENS es un sistema distribuido, abierto y extensible de resolución de nombres. Funciona de la misma manera que las DNS lo hacen con las direcciones IP y los nombres de dominio.

Por ejemplo, el sitio **www.google.com** está en la IP **172.217.16.238** (prueba e pegar esta IP en la barra de direcciones del navegador). Sin embargo nadie se sabe de memoria las IPs de todos los sitios web. Por eso, cuando escribimos www.google.com en el navegador, éste hace una petición a un servidor de DNS, que le devuelve 172.217.16.238 y nos conecta con ese servidor.

```md
www.google.com → 172.217.16.238
```

El ENS funciona de la misma forma. Si queremos enviar activos a una cuenta desde un Wallet, podemos escribir **alicia.eth** en vez de **0x164bC2528baDB8b531aEC305D81B024dcd7294EA**

```md
alicia.eth → 0x164bC2528baDB8b531aEC305D81B024dcd7294EA
```

## El ENS es mucho más

En realidad es muchísimo más.

### Es un NFT

Cada registro es, en realidad un Token que se puede transferir, comprar y vender.

### Soporte para múltiples monedas

El problema de memorizar cuentas no lo tiene sólo Ethereum. Lo tienen todas las demás, pero ENS permite enlazar una cuenta con cuentas de otras Blockchains. Esta es la lista oficial:

* Bitcoin
* Litecoin
* Dogecoin
* Monacoin
* Ethereum
* Ethereum Classic
* Rootstock
* Ripple
* Binance

Con ENS podemos enviar cualquiera de esas monedas a **alicia.eth**.

```md
alicia.eth ┌── 0x164bC2528baDB8b531aEC305D81B024dcd7294EA (Ethereum)
           ├── 1BvBMSEYstWetqTFn5Au4m4GFg7xJaNVN2 (Bitcoin)
           ├── rf1BiGeXwwQoi8Z2ueFYTEXSwuJYfV2Jpn (Ripple)
           └── bnb136ns6lfw4zs5hg4n85vdthaad7hq5m4gtkgf23 (Binance)
```

### Soporte para contenido

Además de monedas, podemos enlazar contenido:

```md
alicia.eth ┌── 0x164bC2528baDB8b531aEC305D81B024dcd7294EA (Ethereum)
           ├── 1BvBMSEYstWetqTFn5Au4m4GFg7xJaNVN2 (Bitcoin)
           ├── rf1BiGeXwwQoi8Z2ueFYTEXSwuJYfV2Jpn (Ripple)
           ├── bnb136ns6lfw4zs5hg4n85vdthaad7hq5m4gtkgf23 (Binance)
           ├── http://alicia.xyz (Sitio Web)
           ├── alicia@gmail.com (Email)
           ├── https://es.gravatar.com/alicia (Avatar)
           ├── Soy Alicia y me gusta pasear por baldosas amarillas (Descripción)
           ├── @aliciamaravilla (Twitter)
           └── aliciamaravilla (GitHub)
```

### Múltiples subdominios

En cada registro se pueden configurar todos los subdominios que se deseen y hacerlos apuntar, tanto a monederos, como a contenido:

```md
donaciones.alicia.eth    → 0x164bC2528baDB8b531aEC305D81B024dcd7294EA
portaforlio.alicia.eth   → http://portafolio.xyz
compañia.alicia.eth      → http://elpaisdelasmaravillas.xyz
```
