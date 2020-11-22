---
name: Quick Start
order: 100
---

# Quick Start

### Setup

**RuntimeDebugAction** is designed to be plug & play, once you imported the package,
a [`Settings`](~/api/BennyKok.RuntimeDebug.Data.Settings.html) ScriptableObject will be created in your project folder `Assets/Resources/`.

Afterward, it's recommended to import TextMeshPro's default resources before play, since some of the asset prefabs uses TextMeshPro.

> [!NOTE]
> If you encountered weird font size of the debug menu after first import, it's because the TextMeshPro's default resource was imported after the prefab's import, you can simply right click on the asset's Prefabs folder and reimport. 

Then you will be good to go!

### Lifecycle

The [`RuntimeDebugSystem`](~/api/BennyKok.RuntimeDebug.Systems.RuntimeDebugSystem.html) is auto injected to you first scene with the [`RuntimeInitializeOnLoadMethod`](https://docs.unity3d.com/ScriptReference/RuntimeInitializeOnLoadMethodAttribute.html) method.

Then the system GameObject with the UI canvas will be set to `DontDestoryOnLoad` and keeps the debug system alive across scene load.


### Menu Interaction
The debug menu have full keyboard navigation and touch input handling at the same time since the UI prefab is using Unity's normal UI component.

> [!NOTE]
> You are required to have a EventSystem in your scene for event interaction (touch,hover,etc..) of the system to work.

**Default Key**

| Key | Description |
| ----------- | ----------- |
| Tab | Toggle Menu, Exit Input |
| Arrow Up/ Down |  Menu Navigation  |
| Enter | Trigger Action, Enter Group, Confirm Input |

<br/>

**Default Action Shortcut Key**

Some default actions has shortcut predefined for ease of access.

| Key | Description |
| ----------- | ----------- |
| L | Toggle Logger |
