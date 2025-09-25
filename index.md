---
title: Welcome to my blog
---

Vivid CarPaint EnvMap Lite – Professional Car Paint Shader Plugin
Welcome to Vivid CarPaint EnvMap Lite, a Unity car paint shader plugin crafted for high-performance vehicle rendering. Inspired by Three.js materials with EnvMap textures, it adds auto-surface AO effects for seamless vehicle-ground integration – ideal for vehicle showcases, mobile projects, or any scene demanding visually stunning yet optimized car paint.

I. Core Advantage: Independent Reflection, No Reflection Probes
Unlike Unity’s traditional reliance on scene lighting and Reflection Probes, this shader uses a self-contained CubeMap-based reflection system:
1. Precision Reflection Control： Assign unique CubeMaps to different vehicle parts (body, wheels, bumpers) for hyper-realistic, customizable reflections – eliminating the unnatural "uniform reflection" from probes.
2. Extreme Performance Optimization：Reflections driven entirely by CubeMaps remove the need for complex real-time lighting, shadows, or Skybox setups. Achieve smooth mobile performance without visual compromise.
II. Key Features
1. Dynamic Color Transition Effect
  ○ Adjust EffectPoint to smoothly shift paint color from base to target hue – perfect for color-changing animations or interactive effects.
  ○ oggle on/off instantly via checkbox.
2. Simulated Surface Ambient Occlusion (AO)
  ○ Fixes the "floating vehicle" illusion by adding ground-to-top gradient occlusion, enhancing weight and grounding.
  ○ Customize AO color/intensity; toggle on/off via checkbox.
  ○ Why it matters: Shadows alone can’t achieve natural scene integration – this fills the gap.
III. Critical Usage Notes
CubeMap quality dictates 70% of results – each vehicle’s unique shape demands tailor-made CubeMaps. Generic maps won’t suffice. 
● Recommendations:
  ○ ✅ Before use: Generate high-quality, vehicle-specific CubeMaps in 3D software (Blender, Maya, 3ds Max).
  ○ ❌ If results disappoint: First optimize your CubeMap assets – this is 90% of the solution (especially for beginners).

IV. Scene Setup Guide
1. For pure vehicle showcases:
  a. Disable Skybox Material
  b. Set Environment Lighting → Source to Gradient (prevents color interference)

2. Performance boost:
  a. Disable lights/shadows entirely (reduces GPU load)

3. Sample scene: See SampleSceneURP (URP-only support)
Note: Demo uses a generic vehicle model (CubeMap mismatch may cause suboptimal visuals – ignore this artifact).

V. Parameter Guide
Material properties are grouped into 4 intuitive sections:
Section	Function	Toggle Support
Color Effect	Controls paint color transitions (e.g., EffectPoint for dynamic hue shifts)	✓ On/Off
Foot AO	Adjusts ground-to-top occlusion gradient (color/intensity)	✓ On/Off
Base	Core material setup (base texture, normal map, AO map)	✗
EnvMap	Assigns reflection CubeMap textures	✗

