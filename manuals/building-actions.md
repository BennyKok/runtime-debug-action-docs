# Building Actions

```csharp
DebugActionBuilder.Button()
    .WithName("Some Action")
    .WithAction(()=>{ });
```

#### Action Type

| Name | Description |
| ---- | ---- |
| Button | OneShot action |
| Toggle | On/Off state action |
| Input | Params input action |