# A toon shader for Unity's terrain tools that works with URP

> ⚠THIS SOLUTION IS BUGGY AND TESTED ONLY ON **MY DEVICE** ONLY IN THE **UNITY EDITOR**⚠

This is an adaptation of [Probably Spoonie's Toon Terrain shader](https://www.youtube.com/watch?v=F_jP3_FKOEE&lc=UgzJG8gfJgI-XClPoHp4AaABAg.9fv08UnOx219lMMJCQED1u) for URP.

When this inhevitably breaks down in the next Unity version, here's a basic explanation of how this works:
- ToonTerrain.shader: changed the includes and dependencies from URP's shaders to the new shaders we cloned.  
  - *(cloned from URP/Shaders/Terrain/TerrainLit.shader)*
- ToonTerrainAdd.shader: this is where we define the new variables we need, like the wall texture, its size, tiling and sampler. also some more includes n stuff  
  - *(clone from URP/Shaders/Terrain/TerrainLitAdd.shader)*
- ToonTerrainInput.hlsl: the variables are defined here again, not sure why (:  
  - *(cloned from URP/Shaders/Terrain/TerrainLitInput.hlsl)*
- ToonTerrainPasses.hlsl: contains the actual calculations. i used here the same triplanar mapping and cutoff algorithms shown in the original video.  
  - *(clone from URP/Shaders/Terrain/TerrainLitPasses.hlsl)*
