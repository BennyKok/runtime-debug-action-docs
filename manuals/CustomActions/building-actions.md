---
name: Building Actions
---

# Building Actions

```csharp
DebugActionBuilder.Button()
    .WithName("Some Action")
    .WithAction(()=>{ });
```

#### Action Type

| Name | Description |
| ---- | ---- |
| Button | One-shot action |
| Toggle | On/Off state action |
| Input | Params input action |
| Flag | Int based value selector action |