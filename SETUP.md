# Contents  
### [Quick Setup](#quick-setup-1)  
### [Detailed Setup](#detailed-setup-1)

# Quick Setup
**[Mods Download](https://github.com/HolographicWings/TOTK-Mods-collection/releases)**
- **Recommended Game Version:** 1.1.2
- **Recommended Mods:**
  - Resolution - SweetMini 1008p - FXAA Off
  - FPS - 60fps Static (Use 30fps Static if you can't reach 60)
  - FPS - DynamicFPS
  - Graphics - Anisotropic Filtering Fix
  - Graphics - LOD Improvement
  - Graphics - Shadows - 1024x
  - Fix - UI Blackscreen Fix
  </br>**BEWARE!** Don't use the Blackscreen Fix if you use any controller UI mod (Playstation/Xbox). In this case use only the version "fix" of the controller mod.

- **Recommended Yuzu Graphics:**
  - Render API: Vulkan
  - Use Disk Pipeline Cache: On
  - Use asynchronous GPU emulation: On
  - Accelerate ASTC Texture Decoding: On
  - Vsync Mode: Mailbox
  - NVDEC emulation: GPU Video Decoding
  - Fullscreen Mode: Exclusive Fullscreen
  - Aspect Ratio: Default (16:9)
  - Resolution: 2x or higher.
  - Window Adapting Filter: Bicubic
  - Anti-Aliasing Method: No AA
  - FSR Sharpness: Don't change

- **Recommended Yuzu Advanced Graphics:**
  - Accuracy Level: Normal
  - ASTC recompression depends on your GPU vRAM:
    - BC1 for 2GB,
    - BC3 for 4-6GB,
    - Uncompressed for more.
  - Enable asynchronous presentation (Vulkan only): Off
  - Force maximum clocks (Vulkan only): Off
  - Decode ASTC textures asynchronously: Off
  - Enable Reactive Flushing: On
  - Use asynchronous shader building: On
    </br>Turn Off if you have weird weapons icons and then right click the game name -> Remove -> Remove Cache Storage.
  - Use Fast GPU Time: Off
  - Use Vulkan Pipeline Cache: On
  - Anisotropic Filtering: x16

- After setup your configurations should look like this example (your settings may vary, read above):

![Recommended Settings](Guide/Readme_Recommendations.png)

- **Ryujinx settings:**
  - Need more documentation

# Detailed Setup
**[Mods Download](https://github.com/HolographicWings/TOTK-Mods-collection/releases)**
- **Recommended Game Version:** 1.1.2
- **Recommended Mods:**
    - Resolution - SweetMini 1008p - FXAA Off (or On, this is personal preference) - Includes FSR and DynRes Disabler - Zero AO Bugs
    - FPS - 60fps Static (use 30fps Static if you can't reach 60fps)
    - FPS - DynamicFPS - Includes Cutscene Fix, Ultrahand Fix - **Do not mix with DynamicFPS++**
    - Fix - UI Blackscreen Fix (unless you are using a controller UI mod, which already has this)
    - Graphics - Anisotropic Filtering Fix - Set AF to 16 in Yuzu advanced graphics settings
    - Graphics - LOD Improvement - Version 2.0 improve LOD while also having a minor performance improvement. More info on the [README](README.md)
    - Graphics - Shadows - 1024x - highest stable (Fix weird shadow flickering and broken Gloom)

- **Recommended Yuzu Graphics:**
  - Render API: Vulkan (OpenGL can have weird visual glitches)
  - Use Disk Pipeline Cache: On
  - Use asynchronous GPU emulation: On
  - Accelerate ASTC Texture Decoding: On
  - Vsync Mode: Mailbox (Or off if you don't mind frame tearing or use any alternate method for avoid it)
  - NVDEC emulation: GPU Video Decoding (This is for cutscenes, try CPU Video Decoding if you have a weak gpu)
  - Fullscreen Mode: Exclusive Fullscreen (Borderless Fullscreen breaks GSYNC)
  - Aspect Ratio: Default (16:9) (Use Strech to Window if using an aspect ratio mod)
  - Resolution: 2x or higher depending on your PC specs. This will multiply the render resolution, in vanilla ToTK it's 1600x900.
  - Window Adapting Filter:
    - Bicubic if the render resolution is above your monitor resolution
    - Bilinear if the render resolution is equal to your monitor resolution
    - FSR if the render resolution is under your monitor resolution
  - Anti-Aliasing Method: No AA or SMAA (FXAA break colors in darkness)
  - FSR Sharpness: Set to taste, this setting only functions when Window Adapting Filter is set to FSR.

- **Recommended Yuzu Advanced Graphics:**
  - Accuracy Level: Normal (High has worse GPU performance, but with a lower risk of visual bugs, TotK does not currently need High except for debugging)
  - ASTC recompression depends on your GPU vRAM:
    - BC1 for 2GB,
    - BC3 for 4-6GB,
    - Uncompressed for more.
  - Enable asynchronous presentation (Vulkan only): Off (framepacing is negatively impacted if you enable, only use if you are 1-2 fps from your locked fps target)
  - Force maximum clocks (Vulkan only): Off (possible small benefit if using very slow or fast hardware, but will waste power efficency)
  - Decode ASTC textures asynchronously: Off ("On" may reduce texture loading stutters, but causes black squares and glitched loading screens)
  - Enable Reactive Flushing: On (Improves syncing of memory)
  - Use asynchronous shader building: On (Greatly reduces stuttering when shaders are compiling. Turn Off if you have weird weapons icons and right click the game name -> Remove -> Remove Cache Storage.)
  - Use Fast GPU Time: Off ("Off" has Higher Accuracy with "Dynamic FPS" and "DynamicFPS++" but for some reason "On" fixed a rare issue where FPS was extremely low and GPU usage extremely High, if you get that issue, try On and report the result to us please)
  - Use Vulkan Pipeline Cache: On (Immense reduction in initial game loading time for AMD, improves shader compilation stutter for NVIDIA and Intel as well)
  - Anisotropic Filtering: x8 or x16 (Will only work if you use the "Anisotropic Filtering Fix" mod, if you experience graphical bugs with an AMD card, switch back to Default)

- **Ryujinx settings:**
  - Really need more documentation
