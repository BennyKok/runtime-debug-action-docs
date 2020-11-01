# 🩺 Runtime Debug Action
Welcome to the documentation for RuntimeDebugAction

<!-- ![RDA Cover](images/rda-as-cover.png) -->

## Overview
**RuntimeDebugAction** is a runtime debug menu system that lets you register and trigger actions in your game development process.

## Features
- Plug & play debug menu system
- Keyboard & Touch input
- Full Keyboard navigation supported
- The menu is built for mobile 
- Action Type
    - Button (Oneshot action)
    - Toggle (On/Off state action)
    - Input (Params input action)
- Mobile Friendly 
- Simple searchable menu
- Fluent API for action registering
- Default debug action 
    - Load scene action 
    - Quality settings actions
    - URP settings actions

## Fluent API
The [`RuntimeDebugSystem`](api/BennyKok.RuntimeDebug.Systems.RuntimeDebugSystem.html) class provide the entry point for registering your custom action, with a Fluent API design, it's a joy to add custom actions. 

```csharp
DebugAction.Button()
    .WithName($"Set {theme.themeName} Theme")
    .WithAction(() =>
    {
        RuntimeDebugSystem.SetTheme(theme, true);
        RuntimeDebugSystem.UIHandler.TogglePanel(true, true);
    })
    .WithPath(themeTag)
);
```