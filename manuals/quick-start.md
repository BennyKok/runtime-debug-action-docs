# Quick Start

### Setup

**RuntimeDebugAction** is designed to be plug & play, once you imported the package,
a [`RDASettings`](../api/BennyKok.RuntimeDebug.Data.Settings.html) ScriptableObject will be created in your project folder `Assets/Resources/`.

Afterward, it's recommended to import TextMeshPro's default resources before play, since some of the asset prefabs uses TextMeshPro.

> [!NOTE]
> If you encountered weird font size of the debug menu after first import, it's because the TextMeshPro's default resource was imported after the prefab's import, you can simplily right click on the assets's Prefabs folder and reimport. 

Then you will be good to go!

### Lifecycle

The [RuntimeDebugSystem](../api/BennyKok.RuntimeDebug.Systems.RuntimeDebugSystem.html) is auto injected to you first scene with the [`RuntimeInitializeOnLoadMethod`](https://docs.unity3d.com/ScriptReference/RuntimeInitializeOnLoadMethodAttribute.html) method.

Then the system GameObject with the UI canvas will be set to `DontDestoryOnLoad` and keeps the debug system alive across scene load.

> [!NOTE]
> You are required to have a EventSystem created in your scene so that the UI interaction of the system will work.

### Menu Interaction
The debug menu have full keyboard navigation and touch input handling at the same time since the UI prefab is using Unity's normal UI component.

##### Default Key

| Key | Description |
| ----------- | ----------- |
| Tab | Toggle Menu |
| Arow Up/ Down |  Menu Navigation  |
| Enter | Trigger Action, Enter Group, Confirm Input |
