# Modular Sprint & Stamina System for Unreal Engine 5

A C++ plugin for Unreal Engine 5 that provides a modular and performant Sprint & Stamina system via an Actor Component. This plug-and-play component can be easily added to any character to manage stamina consumption while sprinting, with easily configurable parameters exposed to Blueprints.

---

## Features

* ✅ **Written entirely in C++** for maximum performance and efficiency.
* ✅ **Plug-and-Play Design:** A self-contained Actor Component that is easy to integrate into any project.
* ✅ **Fully Customizable:** All critical parameters are exposed to Blueprints, allowing for easy tweaking of stamina amounts, drain/regen rates, and sprint speeds without touching the code.
* ✅ **Clean and Optimized:** The code is well-commented and organized, following Unreal Engine's best practices.

---

## Installation

1.  Extract the `StaminaSystem` folder into your project's `Plugins` folder. (Create a `Plugins` folder in your project's root if you don't have one).
2.  Launch your project. The editor should prompt you to build the new plugin module. Click "Yes".
3.  Open the "Plugins" tab inside the Editor (`Edit > Plugins`) and ensure the "Stamina System" plugin is enabled.

---

## How to Use

1.  **Open the Character Blueprint** you want to add the system to.
2.  Click the **`+ Add`** button and search for **`StaminaComponent`**. Select it to add it to your character.
3.  Select the `StaminaComponent` in the Components panel. In the **Details** panel, you can now adjust all the stamina and sprint variables to your liking.
4.  In your Character's **Event Graph**, find your sprint input event (e.g., Left Shift key). Connect the **`Pressed`** pin to the **`StartSprinting`** function from the component, and the **`Released`** pin to the **`StopSprinting`** function.

---

## Customization in the Editor

All properties can be configured in the Details panel of the `StaminaComponent`.

| Property | Description |

* | **Max Stamina** | The maximum amount of stamina the character can have. |
* | **Stamina Drain Rate** | The amount of stamina consumed per second while sprinting. |
* | **Stamina Regen Rate** | The amount of stamina regenerated per second when not sprinting. |
* | **Min Stamina To Sprint**| The stamina threshold required to start sprinting again after it has been depleted. |
* | **Walk Speed** | The character's `MaxWalkSpeed` when not sprinting. This should match your Character Movement settings. |
* | **Sprint Speed** | The character's `MaxWalkSpeed` when sprinting. |

---

## Blueprint API

Functions available to be called from Blueprints.

| Function | Description |

* | **`StartSprinting`** | Attempts to start the sprinting action. Will fail if the character cannot sprint (e.g., not enough stamina). |
* | **`StopSprinting`** | Stops the sprinting action and resets the character's speed to the walk speed. |
* | **`GetCurrentStamina`** | `(Pure)` Returns the current stamina value. Ideal for binding to a UI progress bar. |
* | **`ConsumeStamina`** | Instantly consumes a specific amount of stamina. Useful for other actions like dodging or special abilities. |

<br>

<details>
<summary><strong>Ver em Português 🇧🇷</strong></summary>

# Sistema Modular de Sprint e Stamina para Unreal Engine 5

Um plugin C++ para a Unreal Engine 5 que fornece um sistema modular e performático de Sprint e Stamina através de um Componente de Ator (Actor Component). Este componente plug-and-play pode ser facilmente adicionado a qualquer personagem para gerenciar o consumo de stamina durante a corrida, com parâmetros facilmente configuráveis e expostos para Blueprints.

---

## Funcionalidades

* ✅ **Feito inteiramente em C++** para máxima performance e eficiência.
* ✅ **Design Plug-and-Play:** Um Componente de Ator autocontido, fácil de integrar em qualquer projeto.
* ✅ **Totalmente Customizável:** Todos os parâmetros críticos são expostos para Blueprints, permitindo ajustes fáceis de valores de stamina, taxas de consumo/regeneração e velocidades de corrida sem tocar no código.
* ✅ **Código Limpo e Otimizado:** O código é bem comentado e organizado, seguindo as melhores práticas da Unreal Engine.

---

## Instalação

1.  Extraia a pasta `StaminaSystem` para a pasta `Plugins` do seu projeto. (Crie uma pasta `Plugins` na raiz do seu projeto se ela não existir).
2.  Abra seu projeto. O editor deve perguntar se você deseja compilar o novo módulo do plugin. Clique em "Sim".
3.  Abra a aba "Plugins" dentro do editor (`Edit > Plugins`) e garanta que o plugin "Stamina System" está ativado.

---

## Como Usar

1.  **Abra o Blueprint do Personagem** ao qual você deseja adicionar o sistema.
2.  Clique no botão **`+ Add`** e procure por **`StaminaComponent`**. Selecione-o para adicioná-lo ao seu personagem.
3.  Selecione o `StaminaComponent` no painel de Componentes. No painel **Details**, você agora pode ajustar todas as variáveis de stamina e sprint como desejar.
4.  No **Event Graph** do seu Personagem, encontre seu evento de input para correr (ex: tecla Shift Esquerdo). Conecte o pino **`Pressed`** à função **`StartSprinting`** do componente, e o pino **`Released`** à função **`StopSprinting`**.

---

## Customização no Editor

Todas as propriedades podem ser configuradas no painel Details do `StaminaComponent`.

| Propriedade | Descrição |
| :--- | :--- |
| **Max Stamina** | A quantidade máxima de stamina que o personagem pode ter. |
| **Stamina Drain Rate** | A quantidade de stamina consumida por segundo ao correr. |
| **Stamina Regen Rate**| A quantidade de stamina regenerada por segundo quando não está correndo. |
| **Min Stamina To Sprint**| A quantidade mínima de stamina necessária para começar a correr novamente após ela ter se esgotado. |
| **Walk Speed** | A velocidade (`MaxWalkSpeed`) do personagem quando não está correndo. Deve ser igual à configuração no `Character Movement`. |
| **Sprint Speed** | A velocidade (`MaxWalkSpeed`) do personagem ao correr. |

---

## API para Blueprints

Funções disponíveis para serem chamadas a partir de Blueprints.

| Função | Descrição |

* | **`StartSprinting`** | Tenta iniciar a ação de correr. Falhará se o personagem não puder correr (ex: sem stamina suficiente). |
* | **`StopSprinting`** | Para a ação de correr e redefine a velocidade do personagem para a velocidade de caminhada. |
* | **`GetCurrentStamina`** | `(Pure)` Retorna o valor atual da stamina. Ideal para conectar a uma barra de progresso na UI. |
| **`ConsumeStamina`** | Consome instantaneamente uma quantidade específica de stamina. Útil para outras ações como esquivas ou habilidades especiais. |

</details>
