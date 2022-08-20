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
| natureal00 | bg_village, Town and City | A simple shader that only supports a diffuse channel. A great default shader as it can be affected by lighting, unlike most emissive shaders |
| sfx_55_car01 | stc_gracecar_set, Smashville | A simple shader that supports PRM. This unique shader doesn't require a vertex color set nor a baked lighting map. However, it might ignore shadows and vertex colors |
| a_ring_ironaC | dyr_ring_set, Norfair | A simple shader that supports PRM. This does require a baked channel, but it also supports vertex colors and shadows |
| sfx_55_car01 | stc_grasecar_set, Smashville | A simple shader that only supports a diffuse channel. A great default shader as it can be affected by lighting, unlike most emissive shaders |
| sea_01 | skysea, Tortimer | A great water shader that can support transparency, too! |
| NoBake_Taki_01_mat | chikei, Gaur Plains | A diffuse shader with scrolling uv channel |
| spark | magma wall, Norfair | An emissive shader with scrolling uv channel |
| light04 | ring, PS2 | Useful for most lighting effects that involve a texture with a black background |
| rock_multi | remains, Rathalos Stage | Supports two blended textures, ie grass and rock |
| 40 | sky_dth_set, Hollow Bastion | Supports a normal map for distortion |
| fire | candel fire set, Dracula's Castle | A standard sprite sheet |
| ChandelierFire | lobby_chandelier, Garreg Mach | An emissive shader with distortion. Great for fire! |
| HouseWall | skyloft, Skyloft  | Has a diffuse and a baked lighting channel. This material somehow keeps the performance steady despite Skyloft's 100k+ polygons! |