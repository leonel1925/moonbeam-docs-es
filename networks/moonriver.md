---
title: Moonriver
description: Una descripción general de la configuración actual del despliegue de Moonbeam en Kusama, Moonriver e información sobre cómo comenzar a construir sobre ella usando Solidity.
---

# Moonriver

_Actualizado el 5 de agosto de 2021_

## Meta {: #goal } 

En junio de 2021, Moonriver se lanzó por primera vez como parachain en la red Kusama. Moonriver es una red hermana de Moonbeam y proporciona un entorno para probar código nuevo en condiciones económicas reales. Los desarrolladores ahora tienen acceso para comenzar a experimentar y construir sobre una red canaria incentivada conectada a Kusama. 

Para recopilar la mayor cantidad de comentarios posible y proporcionar una resolución rápida de problemas, hemos configurado un [Discord con un canal Moonriver dedicado](https://discord.gg/5TaUvbRvgM).

## Configuraciones iniciales {: #initial-configurations } 

Moonriver está programado para seguir un [proceso de lanzamiento de 5 fases](https://moonbeam.network/networks/moonriver/launch/). Actualmente, Moonriver se encuentra en la Fase 3 del proceso de lanzamiento y tiene las siguientes configuraciones:

- Funciona como una parachain conectada a la relay chain de Kusama.
- Tiene un conjunto activo de 40 {{ networks.moonriver.staking.max_collators }} collators
- Hay dos puntos finales de RPC (alojados por PureStake). Las personas pueden ejecutar nodos completos para acceder a sus propios puntos finales RPC privados

![Moonriver Diagram](/images/moonriver/moonriver-diagram.png)

Algunas variables / configuraciones importantes a tener en cuenta incluyen:

=== "General"
    |       Variable        |                                    Valor                                     |
    |:---------------------:|:----------------------------------------------------------------------------:|
    |   Precio mínimo de gas   |                 {{ networks.moonriver.min_gas_price }} Gwei*                 |
    |   Tiempo de bloque objetivo   |  {{ networks.moonriver.block_time }} segundos (se espera que sean 6 segundos)  |
    |    Límite de bloque de gas    | {{ networks.moonriver.gas_block }} (se espera que aumente al menos 4x) |
    | Límite de gas de transacción |  {{ networks.moonriver.gas_tx }} (se espera que aumente al menos 4x)   |
    |     RPC endpoint      |                    {{ networks.moonriver.rpc_url }}    }                     |
    |     WSS endpoint      |                       {{ networks.moonriver.wss_url }}                       |

=== "Governance"
    |         Variable         |                                                             Valor                                                              |
    |:------------------------:|:------------------------------------------------------------------------------------------------------------------------------:|
    |      Período de votación      |      {{ networks.moonriver.democracy.vote_period.blocks}} bloques ({{networks.moonriver.democracy.vote_period.days}} días)      |
    | Período de votación acelerada | {{ networks.moonriver.democracy.fast_vote_period.blocks}} bloques ({{networks.moonriver.democracy.fast_vote_period.days}} días) |
    |     Período de promulgación    |     {{ networks.moonriver.democracy.enact_period.blocks}} bloques ({{networks.moonriver.democracy.enact_period.days}} día)      |
    |     Período de reflexión     |      {{ networks.moonriver.democracy.cool_period.blocks}} bloques ({{networks.moonriver.democracy.cool_period.days}} días)      |
    |     Depósito mínimo     |                                    {{ networks.moonriver.democracy.    min_deposit }} MOVR                                     |
    |      Votos máximos       |                                        {{ networks.moonriver.    democracy.max_votes }}                                        |
    |    Propuestas máximas   |                                      {{ networks.moonriver.democracy.    max_proposals }}                                      |

=== "Staking"
    |             Variable             |                                                     Valor                                                     |
    |:--------------------------------:|:-------------------------------------------------------------------------------------------------------------:|
    |     Participación mínima de nominación   |                           {{ networks.moonriver.staking.    min_nom_stake }} tokens                           |
    |        Nominación mínima       |                           {{ networks.moonriver.staking.    min_nom_amount}} tokens                           |
    | Nominadores máximos por collators |                             {{ networks.moonriver.staking.    max_nom_per_col }}                              |
    | Máximo de collators por nominador  |                             {{ networks.moonriver.staking.    max_col_per_nom }}                              |
    |              Ronda              | {{ networks.moonriver.staking.round_blocks }} blocks ({{     networks.moonriver.staking.round_hours }} horas) |
    |          Duración del bono          |                             {{ networks.moonriver.staking.    bond_lock }} rondas                             |

_*Leer más sobre  [denominaciones de tokens](#token-denominations)_

## Empezar {: #get-started } 

--8<-- 'text/moonriver/connect.md'

## Telemetría {: #telemetry } 

Puede ver la información de telemetría actual de Moonriver visitando [este enlace](https://telemetry.polkadot.io/#list/Moonriver).

## Tokens {: #tokens } 

Las fichas de Moonriver también se llamarán Moonriver (MOVR). Visite el sitio de Moonbeam Foundation para obtener más información sobre el [token Moonriver](https://moonbeam.foundation/moonriver-token/). 

### Denominaciones de tokens {: #token-denominations } 

La unidad más pequeña de Moonriver, al igual que Ethereum, es un Wei. Se necesitan 10 ^ 18 Wei para hacer un Moonriver. Las denominaciones son las siguientes:

|      Unit      |   Moonriver (MOVR)   |              Wei              |
|:--------------:|:--------------------:|:-----------------------------:|
|      Wei       | 0.000000000000000001 |               1               |
|    Kilowei     |  0.000000000000001   |             1,000             |
|    Megawei     |    0.000000000001    |           1,000,000           |
|    Gigawei     |     0.000000001      |         1,000,000,000         |
| Micromoonriver |       0.000001       |       1,000,000,000,000       |
| Millimoonriver |        0.001         |     1,000,000,000,000,000     |
|   Moonriver    |          1           |   1,000,000,000,000,000,000   |
| Kilomoonriver  |        1,000         | 1,000,000,000,000,000,000,000 |

## Prueba de participación {: #proof-of-stake } 

En el transcurso del lanzamiento de Moonriver de 5 fases, la red se actualizará progresivamente a una red Proof of Stake completamente descentralizada. Para obtener un desglose de lo que ocurrirá durante cada fase, consulte la página [Estado de lanzamiento de la red](https://moonbeam.network/networks/moonriver/launch/) page.

En la Fase 1, hubo una elección inicial de clasificador para llenar el conjunto de collators activo con partes fuera del equipo Moonbeam. El número de collators en el conjunto activo estará sujeto a la gobernanza. El grupo activo estará formado por los mejores collators por participación, incluidas las nominaciones. 

## Limitaciones {: #limitations } 

Aún no se han incluido algunas [precompilaciones](https://docs.klaytn.com/smart-contract/precompiled-contracts) Puede consultar una lista de precompilaciones compatibles [aquí](/integrations/precompiles/). Sin embargo, todas las funciones integradas están disponibles.
