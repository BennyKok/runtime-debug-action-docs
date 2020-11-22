# 🩺 Runtime Debug Action
Welcome to the documentation for RuntimeDebugAction

![](images/2020-11-21-15-28-50.png)

## Overview
**RuntimeDebugAction** is a runtime debug menu system that lets you register and trigger debug actions with no extra setup. With a set of built-in debug actions and a tiny logger that works out of the box, RDA is built to supercharge your mobile and desktop game development.

> [!WARNING]
> This documentation is still in it's early stages, please notify me if there's anything out of place or not explained well.

## Quick Start

> [!NOTE]
> Take a look at the [➜QuickStart](manuals/QuickStart/index.md) to get started

## Discord

> Join our [💬discord](https://discord.gg/yHHKfNJeUc) server for quick questions and support!

## Features
- Plug & play debug menu system
- Keyboard navigation & touch input
- Full keyboard navigation supported
- Mobile friendly
- [Action Types](~/manuals/CustomActions/index.md#action-type)
    - Button (One-shot action)
    - Toggle (On/Off state action)
    - Input (Params input action)
    - Flag (Int based value selector action)
- Simple searchable menu
- Tiny logger
- [Custom Actions](~/manuals/CustomActions/index.md)
    - Fluent API
    - Debug Action Component
- Support Enter Play Mode Options, faster iteration
- [Default debug action](~/manuals/default-actions.md)

## Fluent API
The [`RuntimeDebugSystem`](api/BennyKok.RuntimeDebug.Systems.RuntimeDebugSystem.yml) class provide the entry point for registering your custom action, with a Fluent API design, it's a joy to add custom actions. 

```csharp
DebugActionBuilder.Button()
    .WithName($"Set {theme.themeName} Theme")
    .WithAction(() =>
    {
        RuntimeDebugSystem.SetTheme(theme, true);
        RuntimeDebugSystem.UIHandler.TogglePanel(true, true);
    })
    .WithGroup("Themes")
);
```

More details of registering actions [here](~/manuals/CustomActions/index.md).