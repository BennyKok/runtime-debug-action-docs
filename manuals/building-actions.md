# Building Actions

```csharp
DebugAction.Button()
    .WithName("Some Action")
    .WithAction(()=>{ });
```

#### Action Type

| Name | Description |
| ---- | ---- |
| Button | Oneshot action |
| Toggle | On/Off state action |
| Input | Params input action |