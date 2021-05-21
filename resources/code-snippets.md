---
title: Fragmentos de Código
description: In order to make it easier to get started with Moonbeam, here are code snippets for each of the tutorials we’ve created.
---

# Fragmentos de Código

## Configuración de un Nodo Moonbeam Local

**Clonar el repositorio de tutoriales de Moonbeam:**

```
git clone -b {{ networks.development.build_tag }} https://github.com/PureStake/moonbeam
cd moonbeam
```

**Instalar Substrate y sus prerrequisitos:**

```
--8<-- 'code/setting-up-node/substrate.md'
```

**Agregar Rust a la ruta del sistema:**

```
--8<-- 'code/setting-up-node/cargoerror.md'
```

**Construir el nodo de desarrollo:**

```
--8<-- 'code/setting-up-node/build.md'
```

**Ejecutar el nodo en modo desarrollo:**

```
--8<-- 'code/setting-up-node/runnode.md'
```

**Depurar la cadena, eliminar todo dato previo, si se ejecutó un nodo en modo desarrollo con anterioridad:**

```
./target/release/moonbeam-development purge-chain --dev
```

**Ejecutar el nodo en modo desarrollo, suprimiendo la información del bloque, excepto los errores de impresión en la consola:**

```
./target/release/moonbeam-development --dev -lerror
```

## Cuenta Génesis

--8<-- 'text/metamask-local/dev-account.md'

## Cuentas de Desarrollo

--8<-- 'text/setting-up-node/dev-accounts.md'

## MetaMask

**Información del nodo de desarrollo de Moonbeam:**

--8<-- 'text/metamask-local/development-node-details.md'

**Moonbase Alpha TestNet:**

--8<-- 'text/testnet/testnet-details.md'
