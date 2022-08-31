---
title: Shaders
subtitle: 
image: "https://w7.pngwing.com/pngs/930/207/png-transparent-pearl-material-sphere-pearl-balloon-download-with-transparent-background-free.png"
alt: 

caption:
  title: Shaders
  subtitle: 
  thumbnail: "https://w7.pngwing.com/pngs/930/207/png-transparent-pearl-material-sphere-pearl-balloon-download-with-transparent-background-free.png"
---

### Quick Tips
Having trouble with alpha channels? Try making sure that "Alpha Sample to Coverage" is set True. You might have to play around with Source and Destination color, too.
Most PRM shaders on PS2's main ring are weird. Their Blue channel, normally dedicated to Ambient Occlusion, actually affects their baked lighting. I recommend avoiding these shaders unless you want to utilize the baked lighting affect.

### Shaders I Use
Here's a few shaders that I like to use, what they could be used for, and where to find them.

| Original Name | Location | Description |
| ----------| ----------| ----------|
| Standard Shaders |
| sfx_naturereal00 | dyr_bg_village_set, Town and City | The most bare bones stage shader. A diffuse channel that supports vertex colors |
| sfx_NoBake_Sand_01 | stc_bg_chikei_set, Gaur Plains | Similar to naturereal but also uses a far render pass |
| SFX_ring_citymetal | dyr_ring_village_set, Town and City | A simple shader that supports PRM. This unique PRM shader doesn't require a baked lighting map |
| a_ring_ironaC | dyr_ring_set, Norfair | A simple shader that supports PRM and shadows. This does require a baked GAO channel that the default white texture can be used to ignore it |
| HouseWall | skyloft, Skyloft  | Has a diffuse and a baked lighting channel. This material somehow keeps the performance steady despite Skyloft's 100k+ polygons! |

| Skybox Shaders | | |
| ----------| ----------| ----------|
| sfx_phonh6_phong3... | far_set, Windy Hill | Emissive Skybox with a scrolling texture |

| Scrolling Textures | | |
| ----------| ----------| ----------|
| NoBake_Taki_01_mat | chikei, Gaur Plains | A diffuse shader with scrolling uv channel |
| spark | magma wall, Norfair | An emissive shader with scrolling uv channel |

| Misc Shaders | | |
| ----------| ----------| ----------|
| sea_01 | skysea, Tortimer | A great water shader that can support transparency, too! |
| light04 | ring, PS2 | Useful for most lighting effects that involve a texture with a black background |
| rock_multi | remains, Rathalos Stage | Supports two blended textures, ie grass and rock |
| fire | candel fire set, Dracula's Castle | A standard sprite sheet |
| ChandelierFire | lobby_chandelier, Garreg Mach | An emissive shader with distortion. Great for fire! |