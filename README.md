# NormalMask-Multi Shader for ME
It's a mod for letting MaterialEditor show corresponding options under the shader, _**Blake/NormalMask Multi**_, on its tab.
The original code of the Unity shaderlab of this shader is on: https://github.com/Blatke/NormalMask-Multi.shader

## Features
**1. Normal Masks** - Supports for importing 5 Normal Masks of which each has three channels (Red, Green, Blue) to separately control the display of the corresponding parts on the normal map. 

**2. Albedo Mask** - Supports for importing a texture as a color mask using its RGB channels to separately control the tint color of the main texture (albedo).

**3. OMS Mask** - Supports for importing a texture as an OMS mask using its RGB channels to separately control the occlusion, metallic and smoothness (glossiness) of the material.

**4. Cutout** - Supports for importing the main texture with alpha channel that indicates the parts on the texture to cull.

## How to Use
Download the **.zipmod** file for the latest version on the [Release](https://github.com/Blatke/NormalMask-Multi-Shader-for-ME/releases) Page, then drag and drop it into your **/mods/** folder to finish installation, or use KKManager to install this mod.

Go to **MaterialEditor** after selecting a particular object in Studio or Chara Maker, choose  _**Blake/NormalMask Multi**_ to substitue the current shader.

Check this video for the detailed demonstration: https://youtu.be/6BTf3i4_je0

To check more details on the options, please go to: https://github.com/Blatke/NormalMask-Multi.shader

## Troubleshooting
When importing a purple normal texture on MaterialEditor in Studio, the bump effect and shadow look weird that it involves artifacts. It's because HS2 / AI-Shoujo, powered by Unity Engine, uses [DXT5nm compression](http://wiki.polycount.com/wiki/Normal_Map_Compression) to treat normal maps, and thus it requires the normal textures imported in runtime should be DXT5nm in which the texture's red and alpha channels are swapped, by which reason the normal texutres we export from Studio by MaterialEditor are usually pink instead of purple. 

The easy way to deal with it is to use some tool like [Normal Map Tool](https://www.patreon.com/posts/99107961) to convert your purple normal textue into a pink DXT5nm one and then import it in the runtime of the game.

## About Me
Bl@ke

Front Page: http://www.blatke.cc

Discord Server: https://discord.gg/nc5pmnf8X3

QQ Chatgroup for Modders: 904857543
