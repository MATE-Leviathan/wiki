# Implementing Blender Models in UE5

## File Format

Use GLB format for static meshes.

## Texture Setup

1. Bake the following maps to 4096x4096(or any arbitrary square dimension) textures:
   - Diffuse
   - Normal
   - Roughness
2. Ensure textures correspond properly to UV maps
3. Save all texture files

## Importing to Unreal Engine

1. Import the GLB model into UE5
2. Create materials with the baked texture maps:
   - Connect Diffuse map
   - Connect Normal map
   - Connect Roughness map

## Important Notes

**Normals**: Planes are single-sided and have no collision by default in UE. This is expected behavior. Ensure your normals are oriented correctly before importing.

**Collision Meshes**: After import, remove collision meshes from all objects except the pool walls. The pool is intentionally split into multiple pieces because automatically generated collision meshes for the full pool would be fully enclosed and non-functional.

