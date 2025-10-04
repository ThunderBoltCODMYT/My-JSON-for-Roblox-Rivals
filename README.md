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

> [!CAUTION]
> USE THEM AT YOUR OWN RISK

---

# My FFlags  
Before you see the Fast Flags important points:
> - It does not matter on which bootstrapper you are using , it will not change how the fast flags take effect.
> - However the amount of FPS you get might differ depending on the bootstrapper you are using.

## Actual JSON Code:
```json
{
    "DFIntTaskSchedulerTargetFps": "5588562",
    "FIntRuntimeMaxNumOfThreads": "2400",
    "FFlagTaskSchedulerLimitTargetFpsTo2402": "False",
    "DFFlagTextureQualityOverrideEnabled": "True",
    "DFIntCullFactorPixelThresholdShadowMapHighQuality": "2147483647",
    "DFIntCullFactorPixelThresholdShadowMapLowQuality": "2147483647",
    "DFIntTextureQualityOverride": "3",
    "FIntDebugForceMSAASamples": "1",
    "FIntRenderGrassDetailStrands": "0",
    "FIntRenderLocalLightFadeInMs": "0",
    "FIntRenderLocalLightUpdatesMax": "1",
    "FIntRenderLocalLightUpdatesMin": "1",
    "FIntRenderShadowIntensity": "0",
    "FIntRenderShadowmapBias": "75",
    "FLogNetwork": "7",
    "FFlagDebugDisplayFPS": "False",
    "FFlagDebugGraphicsPreferD3D11": "True",
    "FFlagDebugGraphicsPreferD3D11FL11": "True",
    "FFlagDisablePostFx": "True",
    "FFlagHandleAltEnterFullscreenManually": "False",
    "FFlagUserHideCharacterParticlesInFirstPerson": "True",
    "DFFlagDebugPauseVoxelizer": "True",
    "DFFlagDebugRenderForceTechnologyVoxel": "True",
    "FIntTerrainArraySliceSize": "0",
    "DFIntDebugFRMQualityLevelOverride": "3",
    "FIntFRMMaxGrassDistance": "0",
    "FIntFRMMinGrassDistance": "0",
    "FFlagDebugForceFSMCPULightCulling": "True",
    "FFlagNewLightAttenuation": "True",
    "FIntDebugTextureManagerSkipMips": "0",
    "FFlagDebugCheckRenderThreading": "True",
    "FFlagDebugForceFutureIsBrightPhase2": "True",
    "FFlagDebugRenderingSetDeterministic": "True",
    "FFlagRenderDebugCheckThreading2": "True",
    "FFlagDebugSkyGray": "True",
    "FIntFontSizePadding": "4",
    "FIntFullscreenTitleBarTriggerDelayMillis": "3600000",
    "FFlagDebugDisableTelemetryEphemeralCounter": "True",
    "FFlagDebugDisableTelemetryEphemeralStat": "True",
    "FFlagDebugDisableTelemetryEventIngest": "True",
    "FFlagDebugDisableTelemetryPoint": "True",
    "FFlagDebugDisableTelemetryV2Counter": "True",
    "FFlagDebugDisableTelemetryV2Event": "True",
    "FFlagDebugDisableTelemetryV2Stat": "True",
    "DFIntConnectionMTUSize": 900,
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

🔧 Order Navigation List

- [Graphics & Rendering](#Graphics-&-Rendering-(Highest-Priority))
- [Engine, Voxel, Terrain, FRM, Threading](#Engine,-Voxel,-Terrain,-FRM,-Threading-(Medium-Priority))
- [Telemetry & Debug Logging](#Telemetry-&-Debug-Logging-(Medium-Priority))
- [Network & CSG (Lower Priority)](#Network-&-CSG-(Lower-Priority))

---

Subsystem-Based Sections (Ordered by Priority)

Graphics & Rendering (Highest Priority)
  
```json
{
  "DFIntTaskSchedulerTargetFps": "5588562",
  "FIntRuntimeMaxNumOfThreads": "2400",
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
  "FFlagDebugGraphicsPreferD3D11FL11": "True",
  "FFlagDebugForceFutureIsBrightPhase2": "True",
  "FFlagDebugForceFSMCPULightCulling": "True",
  "FFlagNewLightAttenuation": "True",
  "FIntDebugTextureManagerSkipMips": "0",
  "FIntFontSizePadding": "4",
  "FIntFullscreenTitleBarTriggerDelayMillis": "3600000"
}
```


Engine, Voxel, Terrain, FRM, Threading (Medium Priority)

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

Telemetry & Debug Logging (Medium Priority)

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

Network & CSG (Lower Priority)

```json
{
  "FLogNetwork": "7",
  "DFIntConnectionMTUSize": 900,
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

<h1>Meaning and effect of every Fast Flag</h1>

🎮 Task Scheduling and Threading
> `DFIntTaskSchedulerFPS` : Sets the target FPS for the task scheduler. A high value like 5588562 effectively removes the FPS cap, allowing the client to run at maximum possible frame rate.  
> `FIntRuntimeMaxNumOfThreads` : Defines the maximum number of threads the runtime can use. Setting this to 2400 enables aggressive multithreading, improving performance on multi-core systems.  
> `FFlagTaskSchedulerLimitTargetFpsTo2402` : When False, disables the internal FPS limit of 2402, allowing full override via `DFIntTaskSchedulerTargetFps`.

🖼️ Graphics & Rendering
- DFFlagTextureQualityOverrideEnabled: Enables manual control over texture quality settings.
- DFIntTextureQualityOverride: Sets the texture quality level. 3 typically corresponds to high quality.
- DFIntCullFactorPixelThresholdShadowMapHighQuality / LowQuality: Maxes out the pixel threshold for shadow map culling, ensuring shadows are always rendered regardless of pixel density.
- FIntDebugForceMSAASamples: Forces Multi-Sample Anti-Aliasing (MSAA) with 1 sample. This can reduce aliasing but may impact performance.
- FIntRenderGrassDetailStrands: Disables grass strand rendering by setting it to 0, improving performance.
- FIntRenderLocalLightFadeInMs: Sets light fade-in time to 0, making lighting transitions instant.
- FIntRenderLocalLightUpdatesMax / Min: Limits local light updates to 1, reducing lighting computation overhead.
- FIntRenderShadowIntensity: Sets shadow intensity to 0, effectively disabling shadows.
- FIntRenderShadowmapBias: Adjusts shadow bias to 75, which can reduce shadow artifacts.
- FFlagDisablePostFx: Disables post-processing effects like bloom and blur, improving clarity and performance.
- FFlagDebugGraphicsPreferD3D11 / D3D11FL11: Forces the client to prefer DirectX 11 rendering, which is more stable and performant on modern systems.
- FFlagDebugSkyGray: Replaces the dynamic skybox with a flat gray sky, reducing GPU load.
- FIntFontSizePadding: Sets padding around fonts, which may affect UI rendering.
- FIntFullscreenTitleBarTriggerDelayMillis: Delays fullscreen title bar triggers. A high value like 3600000 effectively disables it.

🧪 Debug & Determinism
- FFlagDebugDisplayFPS: When False, hides the FPS counter.
- FFlagDebugForceFutureIsBrightPhase2: Forces the newer lighting system for consistency and testing.
- FFlagDebugForceFSMCPULightCulling: Enables CPU-based light culling, which may improve performance in certain scenes.
- FFlagNewLightAttenuation: Enables improved light attenuation calculations for more realistic lighting.
- FIntDebugTextureManagerSkipMips: Controls mipmap skipping. 0 disables skipping, ensuring full texture detail.
- FFlagDebugCheckRenderThreading / RenderDebugCheckThreading2: Enables threading checks for render operations, useful for debugging performance bottlenecks.
- FFlagDebugRenderingSetDeterministic: Forces deterministic rendering behavior, useful for debugging and consistency.
- FFlagHandleAltEnterFullscreenManually: When False, disables manual handling of Alt+Enter fullscreen toggling.
- FFlagUserHideCharacterParticlesInFirstPerson: Hides character particle effects in first-person view, improving visibility and performance.

🧱 Terrain & Voxel
- DFFlagDebugPauseVoxelizer: Pauses the voxelizer, reducing background processing load.
- DFFlagDebugRenderForceTechnologyVoxel: Forces voxel-based rendering, which may simplify lighting and geometry calculations.
- FIntTerrainArraySliceSize: Controls terrain slice size. 0 disables slicing, reducing terrain complexity.
- DFIntDebugFRMQualityLevelOverride: Overrides the FRM (Fast Rendering Mode) quality level. 3 typically corresponds to high quality.
- FIntFRMMaxGrassDistance / MinGrassDistance: Sets grass rendering distance to 0, disabling grass rendering entirely.

📡 Telemetry & Analytics
- FFlagDebugDisableTelemetryEphemeralCounter / Stat / EventIngest / Point / V2Counter / V2Event / V2Stat: Disables various telemetry systems, reducing background data collection and potential performance overhead.

🌐 Networking
- FLogNetwork: Sets network logging level to 7, which is typically verbose for debugging.
- DFIntConnectionMTUSize: Sets the maximum transmission unit size to 900, optimizing packet size for network performance.
- FIntRakNetResendBufferArrayLength: Controls the buffer size for RakNet resends. 128 is a moderate value for stability.
- FFlagOptimizeNetwork / Routing / Transport / ServerTickRate: Enables various network optimizations for routing, transport, and server update frequency.
- DFIntServerPhysicsUpdateRate / ServerTickRate: Sets server update rates to 60Hz, ensuring smooth physics and game logic processing.
- DFIntRakNetResendRttMultiple: Controls resend timing based on round-trip time. 1 is minimal delay.
- DFIntRaknetBandwidthPingSendEveryXSeconds: Sends ping every second for tighter latency tracking.
- DFIntOptimizePingThreshold: Sets ping optimization threshold to 50ms, improving responsiveness.
- DFIntPlayerNetworkUpdateQueueSize / UpdateRate: Controls how often and how much player data is sent over the network.
- DFIntNetworkPrediction / LatencyTolerance / MinimalNetworkPrediction: Fine-tunes prediction and latency handling for smoother movement and sync.

🧱 Geometry & CSG
- DFIntCSGLevelOfDetailSwitchingDistance / L12 / L23 / L34: Controls when level-of-detail (LOD) switches occur for Constructive Solid Geometry. Higher values delay LOD transitions, preserving visual fidelity.

Sources:
GitHub: Roblox Performance FFlags
Roblox DevForum: Fast Flag Allowlist
Bloxstrap FastFlags Guide
Stoofis Fast Flags
Dantezz025/Roblox-Fast-Flags

