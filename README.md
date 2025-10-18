> [!IMPORTANT]
> Fast Flags are internal switches used by Roblox Devs. and Engineers. They are to be used very carefully and only if you know what you are doing. Me myself as an learning roblox engineer wanted to share my FFlags with the community of Roblox. I use these fast flags specifically for Roblox Rivals. If you do not know what you are doing I would strictly reccomend you to **NOT USE** these fast flags.

> [!IMPORTANT]
> ### Fast Flags do not violate the roblox TOS unless they mess with Server logic or exploits

> ### This repository is for educational and testing purposes only and is not endorsed by Roblox Corporation. Use at your own risk.

> [!WARNING]
> ### certain Fast Flags are a bannable offense in some games.

> [!NOTE]
> ### Fast Flags are only used to make client side changes using them for anything like messing with server logic or exploits will get you banned.

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
>>   | `Prefix`               | `DataType` | `Meaning`                          |
>>   |------------------------|------------|------------------------------------|
>>   | `FFlag`                | `Boolean`  | `Fast Flag`                        |
>>   | `FInt`                 | `Int`      | `Fast Integer`                     |
>>   | `FString`              | `String`   | `Fast String`                      |
>>   | `FLog`                 | `Boolean`  | `Fast Log`                         |
>>   | `DFFlag`               | `Boolean`  | `Debug Fast Flag`                  |
>>   | `DFInt`                | `Int`      | `Debug Fast Integer`               |
>>   | `DFString`             | `String`   | `Debug Fast String`                |
>>   | `DFFlag`               | `String`   | `Dynamic Fast Flag`                |
>>   | `SFFlag`               | `Boolean`  | `Studio Fast Flag`                 |
>>   | `SFInt`                | `Int`      | `Studio Fast Integer`              |
>>   | `FFlagDebug`           | `Boolean`  | `Fast Flag for Debugging`          |
>>   | `FFlagUser`            | `Boolean`  | `User-specific Fast Flag`          |
>>   | `FFlagRender`          | `Boolean`  | `Rendering-specific Fast Flag`     |
>>   | `FFlagTaskScheduler`   | `Boolean`  | `Task Scheduler Fast Flag`         |
>>   | `FFlagGraphics`        | `Boolean`  | `Graphics-related Fast Flag`       |
>>   | `FFlagNetwork`         | `Boolean`  | `Network-related Fast Flag`        |
>>   | `FFlagPerf`            | `Boolean`  | `Performance-related Fast Flag`    |
>>   | `DFIntClient`          | `Int`      | `Debug Fast Integer for Client`    |
>>   | `DFIntServer`          | `Int`      | `Debug Fast Integer for Server`    |
>>   | `DFStringTelemetry`    | `String`   | `Debug Fast String for Telemetry`  |  
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
>>>> 
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
>>>> 
>>>🖥️ **User Interface**  
>>>> - FIntGrassMovementReducedMotionFactor  
>>>
>>>⚠️ **Notes**  
>>>> - Any flag not on this list will be ignored, even if injected correctly.  
>>>> - Roblox may update this list at any time without warning.  
>>>> - Roblox Studio is unaffected—you can still use any FastFlags there.  

> [!NOTE]
> I Know my JSON has many of the `FFlags` that are not in the whitelist but I have made this repo just for the purpose that people can atleast test this JSON in rivals and tell me if it gets them better FPS.

# Any BootStrapper in general, How to Use:
1. Open the Bootstrapper Software.
2. Navigate to Fast Flags Editor >> Import Json.
3. Paste in the JSON.
4. Save and your good to go!

# Normal Roblox Bootstrapper How to Use:
1. Navigate to your Roblox Installation directory. Typically found at %localappdata%\Roblox\Versions\ for Windows or C:\Program Files (x86)\Roblox\Versions.
2. Identify the folder version-xxxxxxxxxxxxxxxx containing RobloxPlayerBeta.exe You can do this for Roblox Studio too.
3. Download ClientSettings Folder and put it in folder you opened before
4. Save and your good to go!

```
Roblox Installation Directory
└── Versions
    └── version-xxxxxxxxxxxxxxxx
        ├── RobloxPlayerBeta.exe
        └── ClientSettings
            └── ClientAppSettings.json

```

---

> [!NOTE]
> As of the change made by roblox on September 29, 2025 with that a broader purge was taken to disable most of the engine-level rendering flags if you have been wondering where the fast flags editor option went in bloxstrap this is the reason roblox did this to prevent unauthorised    client-side Manipulation From Roblox's Perspective some fastflags like FIntRenderShadowIntensity were disabled because:
>> - It bypassed their engines intended lighting pipeline.
>> - and could be used to gain unfair performance and visual advantages.
> And because of this when the ui update came in bloxstrap v2.9.1 they removed the fast flag editor and now the latest version is v2.10.0 and they have completely removed the `FFlags` editor option from the ui as a part of this purge Right now it is reccommended that you use any other bootstrapper than bloxstrap but the whitelist however is enforced on all so the fflags not in the whitelist will not work not even if you manually edit ClientSettings.json .

> [!CAUTION]
> USE THEM AT YOUR OWN RISK

> [!NOTE]
> There is a difference between Roblox `ClientSettings.json` syntax and raw `json` syntax for instance:  
> this is how raw `json` syntax looks like:  
> 
> ```json
> {
>     "FFlagDebugSkyGray": true
> }
> ```
> 
> and this is how the Roblox `ClientSettings.json` syntax looks like:
> 
> ```json
> {
>     "FFlagDebugSkyGray": "True"
> }
> ```
> 
> **Differences:**  
> Roblox:  
> - Most of the values in Roblox `ClientSettings.json` are in double quotes "" .
> - and the first letter of the `boolean` values have to be capital - `"True"` / `"False"`  
> - there are some values that do not have to be quoted like `null`, but other than that all of the other values like `booleans`, `strings` and `numbers` have to be quoted.
> 
> Raw:  
> - The values are not in "" .
> - the `boolean` values first letter does not have to be capital - true/false  
> - but again even in raw `json` values like `Numbers`, `booleans`, `null` values, and `arrays` and `objects` dont have to be quoted, while all other values in `strings` have to be quoted in "" .  
> **In this README I am using Roblox's `ClientSettings.json` file `syntax`, however you can use any `syntax` the raw `JSON` `syntax` or Roblox's `ClientSettings.json` `syntax` both will work with no issues.**

---

# Who Should Use This?
This repository is intended for Roblox engineers and advanced power users who understand the implications and risks of modifying Fast Flags. Improper flag usage can destabilize the client or violate game/server policies.

---

# My FFlags  
Before you see the Fast Flags important points:  
> - It does not matter on which bootstrapper you are using , it will not change how the fast flags take effect.  
> - However the amount of FPS you get might differ depending on the bootstrapper you are using.  

## Actual JSON Code:
```json
{
  "DFIntTaskSchedulerTargetFps": "180",
  "FIntRuntimeMaxNumOfThreads": "32",
  "FFlagTaskSchedulerLimitTargetFpsTo2402": "False",
  "FFlagDisablePostFx": "True",
  "FIntRenderShadowIntensity": "0",
  "FIntRenderShadowmapBias": "75",
  "FIntRenderLocalLightUpdatesMax": "1",
  "FIntRenderLocalLightUpdatesMin": "1",
  "FIntRenderLocalLightFadeInMs": "0",
  "FIntRenderGrassDetailStrands": "0",
  "DFIntCullFactorPixelThresholdShadowMapHighQuality": "2147483647",
  "DFIntCullFactorPixelThresholdShadowMapLowQuality": "2147483647",
  "DFIntTextureQualityOverride": "3",
  "DFFlagTextureQualityOverrideEnabled": "True",
  "FIntDebugForceMSAASamples": "1",
  "FFlagDebugGraphicsPreferD3D11": "True",
  "FFlagDebugGraphicsPreferD3D11FL10": "True",
  "FFlagDebugForceFutureIsBrightPhase2": "True",
  "FFlagDebugForceFSMCPULightCulling": "True",
  "FFlagNewLightAttenuation": "True",
  "FIntDebugTextureManagerSkipMips": "0",
  "FIntFontSizePadding": "4",
  "FIntFullscreenTitleBarTriggerDelayMillis": "3600000",
  "DFFlagDebugPauseVoxelizer": "True",
  "DFFlagDebugRenderForceTechnologyVoxel": "True",
  "FIntTerrainArraySliceSize": "0",
  "DFIntDebugFRMQualityLevelOverride": "3",
  "FIntFRMMaxGrassDistance": "0",
  "FIntFRMMinGrassDistance": "0",
  "FFlagDebugRenderingSetDeterministic": "True",
  "FFlagRenderDebugCheckThreading2": "True",
  "FFlagDebugCheckRenderThreading": "True",
  "FFlagDebugDisableTelemetryEphemeralCounter": "True",
  "FFlagDebugDisableTelemetryEphemeralStat": "True",
  "FFlagDebugDisableTelemetryEventIngest": "True",
  "FFlagDebugDisableTelemetryPoint": "True",
  "FFlagDebugDisableTelemetryV2Counter": "True",
  "FFlagDebugDisableTelemetryV2Event": "True",
  "FFlagDebugDisableTelemetryV2Stat": "True",
  "FFlagDebugSkyGray": "True",
  "FFlagDebugDisplayFPS": "False",
  "FFlagUserHideCharacterParticlesInFirstPerson": "True",
  "FFlagHandleAltEnterFullscreenManually": "False",
  "FLogNetwork": "7",
  "DFIntConnectionMTUSize": 1472,
  "FIntRakNetResendBufferArrayLength": "128",
  "FFlagOptimizeNetwork": "True",
  "FFlagOptimizeNetworkRouting": "True",
  "FFlagOptimizeNetworkTransport": "True",
  "FFlagOptimizeServerTickRate": "True",
  "DFIntServerPhysicsUpdateRate": "60",
  "DFIntServerTickRate": "60",
  "DFIntRakNetResendRttMultiple": "1",
  "DFIntRaknetBandwidthPingSendEveryXSeconds": "1",
  "DFIntOptimizePingThreshold": "50",
  "DFIntPlayerNetworkUpdateQueueSize": "20",
  "DFIntPlayerNetworkUpdateRate": "60",
  "DFIntNetworkPrediction": "120",
  "DFIntNetworkLatencyTolerance": "1",
  "DFIntMinimalNetworkPrediction": "0.1",
  "DFIntCSGLevelOfDetailSwitchingDistance": 250,
  "DFIntCSGLevelOfDetailSwitchingDistanceL12": 500,
  "DFIntCSGLevelOfDetailSwitchingDistanceL23": 750,
  "DFIntCSGLevelOfDetailSwitchingDistanceL34": 1000
}
```
---

# 🔧 Order Navigation List

- [Graphics & Rendering (Highest Priority)](#graphics-and-rendering)
- [Engine, Voxel, Terrain, FRM, Threading (Medium Priority)](#Visuals)
- [Telemetry & Debug Logging (Medium Priority)](#Telementry)
- [Network & CSG (Lower Priority)](#network-and-csg)

---

<h1 align="center">Subsystem-Based Sections (Ordered by Priority)</h1>

<h2 id="graphics-and-rendering"> Graphics & Rendering (Highest Priority) </h2>
  
```json
{
  "DFIntTaskSchedulerTargetFps": "180",
  "FIntRuntimeMaxNumOfThreads": "32",
  "FFlagTaskSchedulerLimitTargetFpsTo2402": "False",
  "FFlagDisablePostFx": "True",
  "FIntRenderShadowIntensity": "0",
  "FIntRenderShadowmapBias": "75",
  "FIntRenderLocalLightUpdatesMax": "1",
  "FIntRenderLocalLightUpdatesMin": "1",
  "FIntRenderLocalLightFadeInMs": "0",
  "FIntRenderGrassDetailStrands": "0",
  "DFIntCullFactorPixelThresholdShadowMapHighQuality": "2147483647",
  "DFIntCullFactorPixelThresholdShadowMapLowQuality": "2147483647",
  "DFIntTextureQualityOverride": "3",
  "DFFlagTextureQualityOverrideEnabled": "True",
  "FIntDebugForceMSAASamples": "1",
  "FFlagDebugGraphicsPreferD3D11": "True",
  "FFlagDebugGraphicsPreferD3D11FL10": "True",
  "FFlagDebugForceFutureIsBrightPhase2": "True",
  "FFlagDebugForceFSMCPULightCulling": "True",
  "FFlagNewLightAttenuation": "True",
  "FIntDebugTextureManagerSkipMips": "0",
  "FIntFontSizePadding": "4",
  "FIntFullscreenTitleBarTriggerDelayMillis": "3600000"
}
```
---

<h2 id="Visuals"> Engine, Voxel, Terrain, FRM, Threading (Medium Priority) </h2>

```json
{
  "DFFlagDebugPauseVoxelizer": "True",
  "DFFlagDebugRenderForceTechnologyVoxel": "True",
  "FIntTerrainArraySliceSize": "0",
  "DFIntDebugFRMQualityLevelOverride": "3",
  "FIntFRMMaxGrassDistance": "0",
  "FIntFRMMinGrassDistance": "0",
  "FFlagDebugRenderingSetDeterministic": "True",
  "FFlagRenderDebugCheckThreading2": "True",
  "FFlagDebugCheckRenderThreading": "True"
}
```
---

<h2 id="Telementry"> Telemetry & Debug Logging (Medium Priority) </h2>

```json
{
  "FFlagDebugDisableTelemetryEphemeralCounter": "True",
  "FFlagDebugDisableTelemetryEphemeralStat": "True",
  "FFlagDebugDisableTelemetryEventIngest": "True",
  "FFlagDebugDisableTelemetryPoint": "True",
  "FFlagDebugDisableTelemetryV2Counter": "True",
  "FFlagDebugDisableTelemetryV2Event": "True",
  "FFlagDebugDisableTelemetryV2Stat": "True",
  "FFlagDebugSkyGray": "True",
  "FFlagDebugDisplayFPS": "False",
  "FFlagUserHideCharacterParticlesInFirstPerson": "True",
  "FFlagHandleAltEnterFullscreenManually": "False"
}
```
---

<h2 id="network-and-csg"> Network & CSG (Lower Priority) </h2>

```json
{
  "FLogNetwork": "7",
  "DFIntConnectionMTUSize": 1472,
  "FIntRakNetResendBufferArrayLength": "128",
  "FFlagOptimizeNetwork": "True",
  "FFlagOptimizeNetworkRouting": "True",
  "FFlagOptimizeNetworkTransport": "True",
  "FFlagOptimizeServerTickRate": "True",
  "DFIntServerPhysicsUpdateRate": "60",
  "DFIntServerTickRate": "60",
  "DFIntRakNetResendRttMultiple": "1",
  "DFIntRaknetBandwidthPingSendEveryXSeconds": "1",
  "DFIntOptimizePingThreshold": "50",
  "DFIntPlayerNetworkUpdateQueueSize": "20",
  "DFIntPlayerNetworkUpdateRate": "60",
  "DFIntNetworkPrediction": "120",
  "DFIntNetworkLatencyTolerance": "1",
  "DFIntMinimalNetworkPrediction": "0.1",
  "DFIntCSGLevelOfDetailSwitchingDistance": 250,
  "DFIntCSGLevelOfDetailSwitchingDistanceL12": 500,
  "DFIntCSGLevelOfDetailSwitchingDistanceL23": 750,
  "DFIntCSGLevelOfDetailSwitchingDistanceL34": 1000
}
```

--------------------------

<h1 align="center">Meaning and effect of every Fast Flag</h1>

## Sections Navigation List

- [Task Scheduling and Threading](#task-scheduling-and-threading)  
- [Graphics & Rendering](#graphics--rendering)  
- [Debug & Determinism](#debug--determinism)  
- [Terrain & Voxel](#terrain--voxel)  
- [Telemetry & Analytics](#telemetry--analytics)  
- [Networking](#networking)  
- [Geometry & CSG](#geometry--csg) 

## Task Scheduling and Threading

```json
{
  "DFIntTaskSchedulerTargetFPS" : "180"
}
```

Sets the Target Task Scheduler Frequency to 180 frames per second (FPS). Note: Synchronization with the display's native refresh rate is recommended for optimal frame pacing.

<hr size="1px" width="100%">

```json
{
  "FIntRuntimeMaxNumOfThreads" : "32"
}
```

Defines the Runtime Maximum Thread Pool Size as 32. This aggressively leverages multi-core architectures to maximize parallel processing performance.Note: Set this value to something lower like 16 if you have a low-end cpu which dosent have much threads.

<hr size="1px" width="100%">

```json
{
  "FFlagTaskSchedulerLimitTargetFpsTo2402" : "False"
}
```

Serves as a Task Scheduler Internal Limit Override. Setting it to False disables a hardcoded FPS ceiling of 2402, allowing the `DFIntTaskSchedulerTargetFps` to fully control the execution frequency.

<hr size="1px" width="100%">

## Graphics & Rendering

```json
{
  "DFFlagTextureQualityOverrideEnabled": "True"
}
```

Enables Manual Texture Quality Control, allowing explicit specification of the texture detail level.

<hr size="1px" width="100%">

```json
{
  "DFIntTextureQualityOverride" : "3"
}
```

Sets the Forced Texture Quality Level to 3, which corresponds to the High fidelity preset.

<hr size="1px" width="100%">

```json
{
  "DFIntCullFactorPixelThresholdShadowMapHighQuality": "2147483647",
  "DFIntCullFactorPixelThresholdShadowMapLowQuality": "2147483647"
}
```

`DFIntCullFactorPixelThresholdShadowMapHighQuality` Sets the High-Quality Shadow Map Culling Threshold to its maximum value, effectively preventing the culling of high-quality shadows based on screen-space pixel density and `DFIntCullFactorPixelThresholdShadowMapLowQuality` Sets the Low-Quality Shadow Map Culling Threshold to its maximum value, ensuring low-quality shadows are always rendered.

<hr size="1px" width="100%">

```json
{
  "FIntDebugForceMSAASamples": "1"
}
```

Explicitly sets the Forced Multi-Sample Anti-Aliasing (MSAA) Sample Count to 1, minimizing multi-sampling while potentially reducing certain aliasing forms.

<hr size="1px" width="100%">

```json
{
  "FIntRenderGrassDetailStrands" : "0"
}
```

Disables the rendering of individual Grass Detail Strands to yield a measurable gain in rendering performance. 

<hr size="1px" width="100%">

```json
{
  "FIntRenderLocalLightFadeInMs": "0"
}
```

Sets the Local Light Fade-In Duration to 0 milliseconds, ensuring instantaneous light transitions.

<hr size="1px" width="100%">

```json
{
  "FIntRenderLocalLightUpdatesMax": "1",
  "FIntRenderLocalLightUpdatesMin": "1"
}

```

Limits the Maximum Concurrent Local Light Updates per frame to 1 `FIntRenderLocalLightUpdatesMax`, and sets the Minimum Concurrent Local Light Updates to 1 `FIntRenderLocalLightUpdatesMin`, ensuring a minimal and consistent update frequency to reduce computational load.  

<hr size="1px" width="100%">

```json
{
  "FIntRenderShadowIntensity": "0"
}

```

Sets The Shadow Intensity to 0.

<hr size="1px" width="100%">

```json
{
  "FIntRenderShadowmapBias": "75"
}

```

> [!CAUTION]
> If you set this fflags value to a high number it can cause lighting issues like `Peter Panning`.  
> **What is `Peter Panning`?**  
> In Simple Words `Peter Panning` Is A Lighting Issue Where Objects Look Detached From Their Object Theyve Been Casted By.  
> as this flag is used to change the offset position of a shadow if you set the value to a very high number it can cause this lighting issue.  
> And the opposite of that is `Shadow Acne`.  
> **What Is Shadow Acne?**  
> Shadow acne is a visual artifact manifested as an erroneous pattern of self-shadowing (speckling, stripes, or small-scale noise) appearing  on surfaces that should be smoothly lit or shadowed. It occurs when a point being rendered is incorrectly classified as being in its own  shadow. It happens when you set the value of this above FFlag too low.  
  
Adjusts the Shadow Map Bias Value to 75. This technique is used to mitigate shadow acne artifacts.  

<hr size="1px" width="100%">

```json
{
  "FFlagDisablePostFx": "True"
}

```

Serves as a Post-Processing Pipeline Bypass, disabling effects like Bloom and Depth of Field to improve visual clarity and maximize rendering throughput.

<hr size="1px" width="100%">

```json
{
  "FFlagDebugGraphicsPreferD3D11FL10": "True"
}
```

Forces the client to prefer DirectX 11 rendering, which is more stable and performant on modern systems. 

<hr size="1px" width="100%">

```json
{
  "FFlagDebugSkyGray": "True"
}

```

Replaces the dynamic skybox with a flat gray sky, reducing GPU load. 

<hr size="1px" width="100%">

```json
{
  "FIntFontSizePadding": "4"
}

```

Sets padding around fonts, which may affect UI rendering.  

<hr size="1px" width="100%">

```json
{
  "FIntFullscreenTitleBarTriggerDelayMillis": "3600000"
}

```

Delays fullscreen title bar triggers. A high value like 3600000 effectively disables it.  

<hr size="1px" width="100%">

## Debug & Determinism

```json
{
  "FFlagDebugDisplayFPS": "False"
}

```

When False, hides the FPS counter.

<hr size="1px" width="100%">

```json
{
  "FFlagDebugForceFutureIsBrightPhase2": "True"
}

```

Forces the newer lighting system for consistency and testing.  

<hr size="1px" width="100%">

```json
{
  "FFlagDebugForceFSMCPULightCulling": "True"
}

```

Enables CPU-based light culling, which may improve performance in certain scenes.  

<hr size="1px" width="100%">

```json
{
  "FFlagNewLightAttenuation": "True"
}

```

Enables improved light attenuation calculations for more realistic lighting.  

<hr size="1px" width="100%">

```json
{
  "FIntDebugTextureManagerSkipMips": "0"
}

```

Controls mipmap skipping. 0 disables skipping, ensuring full texture detail. 

<hr size="1px" width="100%">

```json
{
  "FFlagDebugCheckRenderThreading": "True"
}

```

Enables threading checks for render operations, useful for debugging performance bottlenecks.  

<hr size="1px" width="100%">

```json
{
  "FFlagDebugRenderingSetDeterministic": "True"
}

```

Forces deterministic rendering behavior, useful for debugging and consistency.  

<hr size="1px" width="100%">

```json
{
  "FFlagHandleAltEnterFullscreenManually": "False"
}

```

When False, disables manual handling of Alt+Enter fullscreen toggling.  

<hr size="1px" width="100%">

```json
{
  "FFlagUserHideCharacterParticlesInFirstPerson": "True"
}

```

Hides character particle effects in first-person view, improving visibility and performance. 

<hr size="1px" width="100%">
 
## Terrain & Voxel  

```json
{
  "DFFlagDebugPauseVoxelizer": "True"
}

```

Pauses the voxelizer, reducing background processing load.  

<hr size="1px" width="100%">

```json
{
  "DFFlagDebugRenderForceTechnologyVoxel": "True"
}

```

Forces voxel-based rendering, which may simplify lighting and geometry calculations.  

<hr size="1px" width="100%">

```json
{
  "FIntTerrainArraySliceSize": "0"
}

```

Controls terrain slice size. 0 disables slicing, reducing terrain complexity.  

<hr size="1px" width="100%">

```json
{
  "DFIntDebugFRMQualityLevelOverride": "3"
}

```

Overrides the FRM (Fast Rendering Mode) quality level. 3 typically corresponds to high quality.  

<hr size="1px" width="100%">

```json
{
  "FIntFRMMaxGrassDistance": "0",
  "FIntFRMMinGrassDistance": "0"
}
```

Sets grass rendering distance to 0, disabling grass rendering entirely.  

<hr size="1px" width="100%">

## Telemetry & Analytics  

```json
{
  "FFlagDebugDisableTelemetryEphemeralCounter": "True",
  "FFlagDebugDisableTelemetryEphemeralStat": "True",
  "FFlagDebugDisableTelemetryEventIngest": "True",
  "FFlagDebugDisableTelemetryPoint": "True",
  "FFlagDebugDisableTelemetryV2Counter": "True",
  "FFlagDebugDisableTelemetryV2Event": "True",
  "FFlagDebugDisableTelemetryV2Stat": "True"
}

```

Disables various telemetry systems, reducing background data collection and potential performance overhead.  

<hr size="1px" width="100%">

## Networking  

```json
{
  "FLogNetwork": "7"
}

```

Sets network logging level to 7, which is typically verbose for debugging. 

<hr size="1px" width="100%">

```json
{
  "DFIntConnectionMTUSize": 1472
}

```

Sets the maximum transmission unit size to 1472, optimizing packet size for network performance and reduce packet fragmentation.

<hr size="1px" width="100%">

```json
{
  "FIntRakNetResendBufferArrayLength": "128"
}

```

Controls the buffer size for RakNet resends. 128 is a moderate value for stability. 

<hr size="1px" width="100%">

```json
{
  "FFlagOptimizeNetworkRouting": "True",
  "FFlagOptimizeNetworkTransport": "True",
  "FFlagOptimizeServerTickRate": "True",
  "DFIntPlayerNetworkUpdateQueueSize": "20",
  "DFIntPlayerNetworkUpdateRate": "60",
  "DFIntNetworkPrediction": "120",
  "DFIntNetworkLatencyTolerance": "1",
  "DFIntMinimalNetworkPrediction": "0.1"
}
```

Enables various network optimizations for routing, transport, and server update frequency.

<hr size="1px" width="100%">

```json
{
  "DFIntServerPhysicsUpdateRate": "60",
  "DFIntServerTickRate": "60"
}
```

Sets server update rates to 60Hz, ensuring smooth physics and game logic processing.

<hr size="1px" width="100%">

```json
{
  "DFIntRakNetResendRttMultiple": "1"
}

```

Controls resend timing based on round-trip time. 1 is minimal delay. 

<hr size="1px" width="100%">
 
```json
{
  "DFIntRaknetBandwidthPingSendEveryXSeconds": "1"
}

```

Sends ping every second for tighter latency tracking. 

<hr size="1px" width="100%">

```json
{
  "DFIntOptimizePingThreshold": "50"
}

```

Sets ping optimization threshold to 50ms, improving responsiveness.

<hr size="1px" width="100%">

```json
{
  "DFIntPlayerNetworkUpdateQueueSize": "20",
  "DFIntPlayerNetworkUpdateRate": "60"
}

```
 
Controls how often and how much player data is sent over the network. 

<hr size="1px" width="100%">

```json
{
  "DFIntNetworkLatencyTolerance": "1",
  "DFIntMinimalNetworkPrediction": "0.1"
}
```

Fine-tunes prediction and latency handling for smoother movement and sync.  

<hr size="1px" width="100%">

## Geometry & CSG  

```json
{
  "DFIntCSGLevelOfDetailSwitchingDistance": 250,
  "DFIntCSGLevelOfDetailSwitchingDistanceL12": 500,
  "DFIntCSGLevelOfDetailSwitchingDistanceL23": 750,
  "DFIntCSGLevelOfDetailSwitchingDistanceL34": 1000
}

```

These values define the respective CSG Level-of-Detail (LOD) Transition Distances (L0-L1, L1-L2, L2-L3, and L3-L4). The higher values delay LOD switching for Constructive Solid Geometry (CSG), prioritizing visual fidelity over geometric simplification across a greater viewing range.

<hr size="1px" width="100%">

# FFlag Presets
- [`BetterFPS.json`](./BetterFPS.json)
- [`BetterPing.json`](./BetterPing.json)
- [`DisableTelementry.json`](./DisableTelementry.json)

<hr size="1px" width="100%">

# Files already described in the README
- [`RobloxRivalsFFlags.json`](./RobloxRivalsFFlags.json)

<hr size="1px" width="100%">

# The only whitelist FFlags
> [!NOTE]
> you can modify the values in this json as per your choice but do keep in mind that the FFlag `FFlagDebugGraphicsPreferVulkan` causes lighting issues.  
> And also Roblox has clearly said that they can make updates in this whitelist without any prior warning so keep track of the Dev Forum for more changes as I cannot Consistently update this README time-to-time.
> and also this is not a usable preset just to tell you because I literally just copied the fflags from the whitellist and gave them random values you can change the values to make sure there are no errors in your json if you want the whitelist I mentioned it above at the starting of the `README` after some lines or click the link below: `Roblox DevForum: Fast Flag Allowlist`.

- [`Whitelist.json`](./Whitelist.json)

<hr size="1px" width="100%">

Sources & Credit:  
GitHub:  
[stoofis Fast Flags](https://github.com/stoofis/Roblox-Fast-Flags)  
[Dantezz025](https://github.com/Dantezz025/Roblox-Fast-Flags)  
[RBX FFLAGS](https://github.com/Dthesle/RBXFFLAGS)  
[Roblox DevForum: Fast Flag Allowlist](https://devforum.roblox.com/t/allowlist-for-local-client-configuration-via-fast-flags/3966569)  

Update Timestamps : October 5th, 2025(the original date of the creation of this repo.)  
12 October 2025  
16 October 2025  

<hr size="5px" width="100%">
