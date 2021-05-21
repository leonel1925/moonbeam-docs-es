---
title: Glosario
description: We've compiled a glossary of terms related to Polkadot that'll make it easier to learn more about the ecosystem.
---

# Glosario

Existe una gran cantidad de terminología específica de Polkadot, Substrate y del ecosistema emergente Parity/Web3. Hemos confeccionado una lista de términos que creemos todos querrán saber al consultar la documentación, los planes y los tutoriales de Moonbeam.

### Intercaladores

Son unos de los participantes principales de la red, necesarios para soportar las parachains dentro de la Red Polkadot. En Moonbeam, los intercaladores son los nodos responsables de la producción de bloques y de la presentación de los bloques producidos en la Cadena de Relevos de Polkadot, para que sean finalizados.

### Nominadores

Son los poseedores de tokens que optan por “respaldar” a un validador. Pueden recibir parte de la recompensa del validador, pero serán susceptibles de sufrir un recorte en sus tokens invertidos, en caso de mal comportamiento por parte del validador. Un nominador puede respaldar hasta 16 validadores y las obligaciones se distribuyen íntegramente entre los validadores respaldados que fueran seleccionados para el conjunto de validadores. Si desea nominar PureStake para Polkadot y/o Kusama, por favor siga las instrucciones de [esta guía](https://www.purestake.com/technology/polkadot-validator/).

### Prueba de Participación Nominada

Es el mecanismo utilizado por Polkadot para seleccionar su conjunto de validación de bloque para optimizar la seguridad de la cadena. Básicamente, es un sistema de Prueba de Participación (PoS, por su sigla en inglés) en el que los nominadores respaldan a los validadores. Se seleccionan los validadores con mayor respaldo para ser parte del conjunto validador por una sesión. En caso de mal comportamiento, se recortará la participación del validador. Por ende, se espera que los nominadores realicen las diligencias debidas sobre los validadores que nominan. Si desea nominar PureStake para Polkadot y/o Kusama, por favor siga las instrucciones de [esta guía](https://www.purestake.com/technology/polkadot-validator/).

### Parachains

Es una cadena de bloques que tiene una ranura y que está conectada a Polkadot. Las parachains reciben seguridad compartida de Polkadot y la capacidad de interacción con otras parachains de la red Polkadot. Deben bloquear DOT, el token de la cadena de relevos nativo, para asegurar una ranura por un período de tiempo determinado (hasta dos años).

### Parathreads

Es una cadena de bloques que se puede conectar a Polkadot. Las parathreads son capaces de interactuar con otros miembros de la red Polkadot, pero compiten bloque por bloque por la finalización de bloque (en DOT). Compiten con otras parathreads por la finalización de bloque, lo cual significa que se seleccionará el bloque con mayor oferta para ser finalizado en dicha ronda.

### Polkadot

Es una red de cadenas de bloques conectadas que suministra seguridad compartida y la capacidad de interacción entre las cadenas. Polkadot es diseñado utilizando el marco de desarrollo Substrate. Se llama parachains a las cadenas que se conectan a Polkadot.

### Cadena de Relevos

Es la cadena de bloque central que soporta a la red Polkadot. Las parachains se conectan a la Cadena de Relevos y la utilizan para la seguridad compartida y para la transmisión de mensajes. Los validadores en la Cadena de Relevos ayudan a asegurar las parachains.

### Contratos Inteligentes

Un contrato inteligente es un programa informático o un protocolo de transacción ideado para ejecutar, controlar o documentar automáticamente eventos o acciones legalmente relevantes, de conformidad con los términos de un contrato o acuerdo. Los contratos inteligentes pretenden reducir la necesidad de intermediarios confiables, de arbitraciones y los costos de ejecución, así como la reducción de pérdidas por fraude y excepciones accidentales y maliciosas. [Más infomación](https://en.wikipedia.org/wiki/Smart_contract).

### Substrate

Es un marco de desarrollo de cadena de bloque basado en Rust, creado por Parity Technologies, que se basó en su experiencia implementando para múltiples clientes de cadena de bloque. Substrate consta de varios módulos y funcionalidades necesarias para la construcción de una cadena de bloque, incluidos la red entre pares (P2P, por su sigla en inglés), los mecanismos de consenso, el staking, la criptomoneda, los módulos de gobernanza en cadena, entre otros. Reduce drásticamente los tiempos y los esfuerzos de ingeniería requeridos para implementar una cadena de bloque.

### Substrate Frame Pallets

Los Substrate Frame Pallets son una colección de módulos basados en Rust, que suministran la funcionalidad necesaria para construir una cadena de bloque. 

### Validadores

Es un nodo que asegura la Cadena de Relevos de Polkadot al invertir DOT en la red y que puede sufrir un recorte por mal comportamiento. Finalizan bloques desde los intercaladores en las parachains y también participan del consenso para el próximo bloque de Cadena de Relevo, junto con otros validadores.

### WebAssembly/Wasm

WebAssembly es un estándar abierto que define un formato portable de código binario. Es soportado por diferentes lenguajes de programación, compiladores y navegadores.
