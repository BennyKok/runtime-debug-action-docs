---
name: Adding Actions
order: 90
---

# Adding Actions

## Overview

Adding custom debug action to your game is extremely easy, and you have two options

1. [Fluent API](#fluent-api)
2. [Debug Action Component](#debug-action-component)

## Fluent API

The [`DebugActionBuilder`](~/api/BennyKok.RuntimeDebug.Actions.DebugActionBuilder.yml) is the builder class for creating actions.

```csharp
var debugAction = DebugActionBuilder.Button()
    .WithName("Some Action")
    .WithAction(()=>{ });
```

For a full list of common [Fluent APIs](~/api/BennyKok.RuntimeDebug.Actions.FluentAction-1.yml)

### Register Actions

To register any actions

```csharp
RuntimeDebugSystem.RegisterActions(
    DebugActionBuilder.Button()
        .WithName("Your actions")
);
```
> [!WARNING]
> To prevent any ghost action hanging in the debug menu, it's suggested to handle your actions' unregistration if they were added from any `MonoBehaviour`, e.g. 
> 1. Register actions in the `OnEnable` and unregister actions in the `OnDisable`
> 2. Register actions in the `OnAwake` and unregister actions in the `OnDestroy`

### Unregister Actions

There are few ways to remove actions from the system

#### By group

If you have defined custom path for you actions via `WithGroup("YourGroup")` or the argument `group` in the `RegisterActions` method, you can do as below to remove the actions with same path.

```csharp
RuntimeDebugSystem.UnregisterActionsByGroup(
    "YourGroup"
);
```

#### By references

If you have references to you actions, you can pass them into the `RuntimeDebugAction.UnregisterActions` method directly.

#### By ID

If you have defined a ID for your actions via `WithId("YourId")`, you can do as below to remove the actions with the same ID.

```csharp
RuntimeDebugSystem.UnregisterActionsById(
    "YourId"
);
```



## Debug Action Component

![](../../images/2020-11-22-14-35-25.png)

You can define the action name, group, description, etc...

The Unity Action is the `UnityEvent` callback from the menu

![](../../images/2020-11-22-14-36-34.png)

The action will automatically appeared in the debug menu

![](../../images/2020-11-22-14-38-47.png)


#### Action Type

| Name | Description |
| ---- | ---- |
| [`Button`](~/api/BennyKok.RuntimeDebug.Actions.DebugActionButton.yml) | One-shot action |
| [`Toggle`](~/api/BennyKok.RuntimeDebug.Actions.DebugActionFlag.yml) | On/Off state action |
| [`Input`](~/api/BennyKok.RuntimeDebug.Actions.DebugActionInput.yml) | Params input action |
| [`Flag`](~/api/BennyKok.RuntimeDebug.Actions.DebugActionFlag.yml) | Int based value selector action |