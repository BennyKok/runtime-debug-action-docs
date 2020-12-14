---
name: Custom Actions
order: 90
---

# Custom Actions

## Overview

Adding custom debug action to your game is extremely easy, and you have three options

1. [Attribute Reflection](attribute-reflection.md)
2. [Fluent API](fluent-api.md)
3. [Debug Action Component](debug-action-component.md)


#### Action Type

| Name | Description |
| ---- | ---- |
| [`Button`](~/api/BennyKok.RuntimeDebug.Actions.DebugActionButton.yml) | One-shot action |
| [`Toggle`](~/api/BennyKok.RuntimeDebug.Actions.DebugActionFlag.yml) | On/Off state action |
| [`Input`](~/api/BennyKok.RuntimeDebug.Actions.DebugActionInput.yml) | Params input action |
| [`Flag`](~/api/BennyKok.RuntimeDebug.Actions.DebugActionFlag.yml) | Int based value selector action |
| [`Enum`](~/api/BennyKok.RuntimeDebug.Actions.DebugActionEnum.yml) | Enum based selector action |