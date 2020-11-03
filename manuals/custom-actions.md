# Custom Actions

### Overview

The most common thing you are going to do is adding custom debug action that is sepecific to your game, and with the Fluent API design, it's extremely easy.

### Building Actions

```csharp
DebugAction.Button()
	.WithName("Some Action")
	.WithAction(()=>{ });
```

#### Action Type

| Name | Description |
| ---- | ---- |
| Button | |
| Toggle | |
| Input | |

### Registering Actions

To register any actions

```csharp
RuntimeDebugSystem.RegisterActions(
	...Your actions here...
);
```