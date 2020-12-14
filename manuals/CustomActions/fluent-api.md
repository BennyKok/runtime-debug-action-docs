---
name: Fluent API
order: 50
---

# Fluent API

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
> [!NOTE]
> To prevent any ghost action hanging in the debug menu, it's suggested to handle your actions' unregistration if they were added from any `MonoBehaviour` and maybe disabled or destroy in future, e.g. 
> 1. Register actions in the `OnAwake` and unregister actions in the `OnDestroy`
> 2. Register actions in the `OnEnable` and unregister actions in the `OnDisable`


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