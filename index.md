---
title: Welcome to my blog
---

### **Vivid CarPaint EnvMap Lite – Professional Car Paint Shader Plugin**
Welcome to Vivid CarPaint EnvMap Lite, a Unity car paint shader plugin crafted for high-performance vehicle rendering. Inspired by Three.js materials with EnvMap textures, it adds auto-surface AO effects for seamless vehicle-ground integration – ideal for vehicle showcases, mobile projects, or any scene demanding visually stunning yet optimized car paint.

![](https://cdn.nlark.com/yuque/0/2025/png/654181/1758813420888-c5832f8b-f73f-4f96-b1ee-184f3b3aa6d5.png)

#### **I. Core Advantage: Independent Reflection, No Reflection Probes**
Unlike Unity’s traditional reliance on scene lighting and Reflection Probes, this shader **uses a self-contained CubeMap-based reflection system**:

1. **Precision Reflection Control**： Assign unique CubeMaps to different vehicle parts (body, wheels, bumpers) for hyper-realistic, customizable reflections – eliminating the unnatural "uniform reflection" from probes.
2. **Extreme Performance Optimization**：Reflections driven entirely by CubeMaps remove the need for complex real-time lighting, shadows, or Skybox setups. Achieve smooth mobile performance without visual compromise.

#### **II. Key Features**
1. **Dynamic Color Transition Effect**
    - Adjust **EffectPoint **to smoothly shift paint color from base to target hue – perfect for color-changing animations or interactive effects.
    - oggle on/off instantly via checkbox.
2. **Simulated Surface Ambient Occlusion (AO)**
    - Fixes the "floating vehicle" illusion by adding ground-to-top gradient occlusion, enhancing weight and grounding.
    - Customize AO color/intensity; toggle on/off via checkbox.
    - Why it matters: Shadows alone can’t achieve natural scene integration – this fills the gap.

#### **III. Critical Usage Notes**
:::danger
CubeMap quality dictates 70% of results – each vehicle’s unique shape demands tailor-made CubeMaps. Generic maps won’t suffice. 

:::

+ Recommendations:
    - ✅ **Before use:** Generate high-quality, vehicle-specific CubeMaps in 3D software (Blender, Maya, 3ds Max).
    - ❌** If results disappoint:** First optimize your CubeMap assets – this is 90% of the solution (especially for beginners).



#### IV. Scene Setup Guide
1. For pure vehicle showcases:
    1. Disable Skybox Material
    2. Set Environment Lighting → Source to Gradient (prevents color interference)

![](https://cdn.nlark.com/yuque/0/2025/png/654181/1758813549416-b0688361-eff8-4d30-9426-70ef395df821.png)

2. Performance boost:
    1. Disable lights/shadows entirely (reduces GPU load)

![](https://cdn.nlark.com/yuque/0/2025/png/654181/1758813683552-ccaa6bac-33a5-4664-a985-6ba89f1dfe59.png)

3. Sample scene: See SampleSceneURP (URP-only support)

:::danger
Note: Demo uses a generic vehicle model (CubeMap mismatch may cause suboptimal visuals – ignore this artifact).

:::

![](https://cdn.nlark.com/yuque/0/2025/png/654181/1758814999190-a777550d-5662-4838-bb05-341795f675b8.png)

#### **V. Parameter Guide**
Material properties are grouped into 4 intuitive sections:

| <font style="color:#000000;">Section</font> | <font style="color:#000000;">Function</font> | <font style="color:#000000;">Toggle Support</font> |
| --- | --- | --- |
| <font style="color:#000000;">Color Effect</font> | <font style="color:#000000;">Controls paint color transitions (e.g., EffectPoint for dynamic hue shifts)</font> | <font style="color:#000000;">✓ On/Off</font> |
| <font style="color:#000000;">Foot AO</font> | <font style="color:#000000;">Adjusts ground-to-top occlusion gradient (color/intensity)</font> | <font style="color:#000000;">✓ On/Off</font> |
| <font style="color:#000000;">Base</font> | <font style="color:#000000;">Core material setup (base texture, normal map, AO map)</font> | <font style="color:#000000;">✗</font> |
| <font style="color:#000000;">EnvMap</font> | <font style="color:#000000;">Assigns reflection CubeMap textures</font> | <font style="color:#000000;">✗</font> |


![](https://cdn.nlark.com/yuque/0/2025/png/654181/1758815258503-134c28fb-1ec9-47a2-b797-59d7d340d2e4.png)




