> [!IMPORTANT]
> Fast Flags are internal switches used by Roblox Devs. and Engineers. They are to be used very carefully and only if you know what you are doing. Me myself as an learning roblox engineer wanted to share my FFlags with other people. I use these fast flags specifically for Roblox Rivals. If you do not know what you are doing I would strictly reccomend you to NOT USE these fast flags.

> [!IMPORTANT]
> **Fast Flags do not violate the roblox TOS unless they mess with Server logic or exploits**

> [!WARNING]
> **certain Fast Flags are a bannable offense in some games.**

> [!NOTE]
> **Fast Flags are only used to make client side changes using them for anything like messing with server logic or exploits will get you banned.**

> [!TIP]
> What exactly are Fast Flags and custom mods and what do they do? How do they help us?
>
> What Are Fast Flags?  
>> Fast Flags are internal configuration switches used by Roblox to control engine behavior. Think of them as hidden toggles that developers use to:
>> - Enable or disable features
>> - Set performance thresholds
>> - Control rendering, physics, networking, and more
>> They’re not exposed in the regular settings UI, but they exist deep in the engine, often as FFlag, DFInt, FInt, or DFFlag keys.
>
> There are many different prefixes and all have their own meanings:
>>   | `Prefix`               | `Meaning`                                 |
>>   |------------------------|-------------------------------------------|
>>   | `FFlag`                | `Fast Flag`                               |
>>   | `FInt`                 | `Fast Integer`                            |
>>   | `FString`              | `Fast String`                             |
>>   | `FLog`                 | `Fast Log`                                |
>>   | `DFFlag`               | `Debug Fast Flag`                         |
>>   | `DFInt`                | `Debug Fast Integer`                      |
>>   | `DFString`             | `Debug Fast String`                       |
>>   | `DFFlag`               | `Dynamic Fast Flag`                       |
>>   | `SFFlag`               | `Studio Fast Flag`                        |
>>   | `SFInt`                | `Studio Fast Integer`                     |
>>   | `FFlagDebug`           | `Fast Flag for Debugging`                 |
>>   | `FFlagUser`            | `User-specific Fast Flag`                 |
>>   | `FFlagRender`          | `Rendering-specific Fast Flag`            |
>>   | `FFlagTaskScheduler`   | `Task Scheduler Fast Flag`                |
>>   | `FFlagGraphics`        | `Graphics-related Fast Flag`              |
>>   | `FFlagNetwork`         | `Network-related Fast Flag`               |
>>   | `FFlagPerf`            | `Performance-related Fast Flag`           |
>>   | `DFIntClient`          | `Debug Fast Integer for Client`           |
>>   | `DFIntServer`          | `Debug Fast Integer for Server`           |
>>   | `DFStringTelemetry`    | `Debug Fast String for Telemetry`         |  
>
> What Are Custom Mods?  
>> Custom mods are user-defined configurations that override default FastFlag values. These mods are:
>> - Written in JSON or injected via tools like Bloxstrap
>> - Designed to optimize performance, reduce latency, or disable unwanted effects
>> - Often tailored for specific hardware (e.g. legacy CPUs, low-end GPUs)
>> Mods let you take control of the engine—not just play the game, but engineer it.
>
> Why Should we use Fast Flags?  
>> Well There are Several Reasons:  
>> - Unlock the most fps you can out of your machine.  
>> - Lower Latency.  
>> - Disable PostFX.  
>> - Optimize Roblox According To Your Hardware.  
>> - Network Tweaks.  

> [!NOTE]
> I have described what all of these fast flags do at the end.

> [!NOTE]
> September 29, 2025 changes made:
>> Roblox has decided to make a huge change on September 29 of 2025.  
>> On September 29, 2025, Roblox officially introduced the FastFlag Allowlist—a system that restricts which FastFlags can be used in ClientAppSettings.json. Any flag not on the allowlist is now silently ignored by the client.
“FastFlags is a beloved but also often misused feature… increasingly a contributing factor to cheating and abuse… can destabilize the client to the point that a re-installation is required.” — Roblox DevForum  
>> Why Roblox did this?  
>>Roblox cited several reasons:
>>> - Security: Some flags could be used to manipulate rendering or threading in ways that gave unfair advantages or exposed vulnerabilities.
>>> - Stability: Misused flags could crash the client or cause unpredictable behavior.
>>> - Support burden: Players using broken configs often blamed Roblox for bugs they caused themselves.
>>> - Cheating prevention: Certain flags were exploited to disable visual effects, improve visibility, or bypass performance limits.  
>>
>> What got purged?  
>>> Most of the following categories were hit hard:
>>> - Rendering flags: Shadow intensity, post-processing, lighting tweaks.
>>> - Scheduler flags: FPS caps, threading control.
>>> - Debug flags: Internal tools like FFlagDebugDisplayFPS, FFlagDebugCheckRenderThreading.
>>> - Experimental tech flags: Vulkan, OpenGL, Future Is Bright phases.
>>> Only a small set of flags survived—mostly safe toggles like fullscreen behavior, texture quality, and MSAA samples.
>>
>> a Small Whitelist of about 20~ validated fast flags exist:  
>>> These are the flags Roblox currently allows in ClientAppSettings.json:  
>>>🧱 **Geometry**
>>>> - DFIntCSGLevelOfDetailSwitchingDistance
>>>> - DFIntCSGLevelOfDetailSwitchingDistanceL12
>>>> - DFIntCSGLevelOfDetailSwitchingDistanceL23
>>>> - DFIntCSGLevelOfDetailSwitchingDistanceL34
>>>🎨 **Rendering**
>>>> - FFlagHandleAltEnterFullscreenManually
>>>> - DFFlagTextureQualityOverrideEnabled
>>>> - DFIntTextureQualityOverride
>>>> - FIntDebugForceMSAASamples
>>>> - DFFlagDisableDPIScale
>>>> - FFlagDebugGraphicsPreferD3D11
>>>> - FFlagDebugSkyGray
>>>> - DFFlagDebugPauseVoxelizer
>>>> - DFIntDebugFRMQualityLevelOverride
>>>> - FIntFRMMaxGrassDistance
>>>> - FIntFRMMinGrassDistance
>>>> - FFlagDebugGraphicsPreferVulkan
>>>> - FFlagDebugGraphicsPreferOpenGL
>>>🖥️ **User Interface**
>>>> - FIntGrassMovementReducedMotionFactor
>>>
>>>⚠️ **Notes**
>>>> - Any flag not on this list will be ignored, even if injected correctly.
>>>> - Roblox may update this list at any time without warning.
>>>> - Roblox Studio is unaffected—you can still use any FastFlags there.

> [!NOTE]
> I Know my JSON has many of the `FFlags` that are not in the whitelist but I have made this repo just for the purpose that people can atleast test this JSON in rivals and tell me if it gets them better FPS.

# Bloxstrap or any BootStrapper in general, How to Use:
1. Open the [Bloxstrap Menu](https://github.com/pizzaboxer/bloxstrap).
2. Navigate to Fast Flags >> Fast Flags Editor >> Import Json.
3. Paste in the JSON.
4. Save and your good to go!

> [!CAUTION]
> USE THEM AT YOUR OWN RISK  
<hr size="5px" width="100%">
<html>
  <body>
    <h1>My FFlags</h1>
    <p>Before this, I just wanna say that you can use any bootstrapper you want bloxstrap, Plexity, FishTrap, FrostStrap but either way it will not change how the <code>FFlags</code> take effect, however the amount of fps you get may be different depending on the bootstrapper you are using.</p>
  </body>
</html>
