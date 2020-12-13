---
name: VR Setup
---

# VR Setup

> [!WARNING]
> Beta support VR, currently only tested for
> - XR Interaction Toolkit
> - Oculus Integration

RDA comes with a specialized UI prefab for VR target. Which has a world space UI made for VR usage, it also contains a scripts to automatically orient the debug menu to your looking direction with smooth damping.

The customized UI prefab, adds the framework specific Graphic Raycaster for all the Canvas components in the prefab.

- ![](../../images/2020-12-06-15-39-31.png)<br/>Used by XR Interaction Toolkit

- ![](../../images/2020-12-06-15-45-00.png)<br/>Used by Oculus Integration

Which if are you using other VR input framework, you might need to replace the Graphic Raycaster in the prefab to the one specified in that specific framework.

### VR Menu Toggle

With VR device, the default input action of toggling the menu has been set to pressing the two secondary button on both of your controller at the same time, so for Quest controller, is the two "Y" button. Which will require Unity's Input System. However, you can rebind the shortcut to other input from the RDASettings.

## Using XR Interaction Toolkit

https://github.com/Unity-Technologies/XR-Interaction-Toolkit-Examples

If you starting off with Unity's XR Interaction Toolkit, RDA already comes with a settings preset for the XR Interaction Toolkit, and since the XR Interaction Toolkit is now using the InputSystem, head over the RDASettings and apply the "RDASettings InputSystem XR" preset.

![](../../images/2020-12-06-15-18-47.png)

![](../../images/2020-12-06-15-21-20.png)

### Default Input

With XR Interaction Toolkit, the default trigger action is with the trigger button on your controller while you use the controller pointer like on the mobile touch screen.

### XR Device Simulator

If you don't have device to test, you can use the "XR Device Simulator"

![](../../images/2020-12-06-15-26-58.png)

From UPM, import "XR Device Simulator" from the samples, then drag and drop the simulator into the scene. 

![](../../images/2020-12-06-15-27-40.png)

Everything should be ready to go.

![](../../images/2020-12-06-15-28-56.png)

## Using Oculus Integration

If you are using Oculus Integration instead, apply the "RDASettings InputSystem VR Oculus" preset.

If you are not familiar with Oculus Integration, read more on Oculus Developer site https://developer.oculus.com/documentation/unity/unity-import/

![](../../images/2020-12-06-15-42-20.png)

And you will need to also activate the new Input System with Oculus Integration, make sure it is set to both.

![](../../images/2020-12-06-15-43-29.png)

### Default Input

With Oculus Integration, the default trigger action is with the "A" button (primary button) on your controller while you use the controller pointer like on the mobile touch screen.