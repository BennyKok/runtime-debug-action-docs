# Unregistering Actions

There are few ways to remove actions from the system

## By path

If you have defined custom path for you actions via `WithPath("YourPath")` or the argument `path` in the `RegisterActions` method, you can do as below to remove the actions with same path.

```csharp
RuntimeDebugSystem.UnregisterActionsByPath(
    "YourPath/"
);
```

## By references

If you have references to you actions, you can pass them into the `RuntimeDebugAction.UnregisterActions` method directly.

## By id

If you have defined a id for your actions via `WithId("YourId")`, you can do as below to remove the actions with the same id.

```csharp
RuntimeDebugSystem.UnregisterActionsById(
    "YourId"
);
```