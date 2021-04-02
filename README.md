# PlanetWalker
Simple game to learn Godot engine and 3d modeling techniques along with producing synth soundtrack for games. Gamer will control rover to find crystals on planet surface. Be ready to accept challenge splitted by many levels.

## Why voxel art?
Easy to create, fun to work and beatiful to look. But for me personally voxel art is a way to transform pixel art experience from 90-s to modern 3D world.

## Mesh libraries in Godot
Mesh libraries is core technique in this game which make possible to quickly and easily generate levels from prepared set of meshes. Usage of MeshLibrary object in Godot is not really trivial but is not rocket science same time. You need to keep in mind 3 important points:
1. To export scene as mesh library you should create new scene from nowhere (Scene->New Scene), such scene must not have any root scene or root nodes. Although it is ok to save such scene to separate tscn file.
2. Avoid creation of separate material for your object along with mesh - such material will not be exported to MeshLibrary and you will get mesh without texture, instead of that add material to mesh directly (Inspector -> Mesh -> Edit -> Surface 1 -> Material).
3. And finally to create new MeshLibrary - Scene -> Convert to... -> Mesh library, in dialog enter name of file with MeshLibrary, don't forget to enter meshlib extension or you will get error.
To use prepared set of meshes you need to add GridMap to your scene and choose MeshLibrary for it (also work to drag meshlib file from FileSystem tab to MeshLibrary property of GridMap object.

## Toolset
https://www.voxelmade.com/magicavoxel/ - opens ource very useful tool to create voxel models.

https://godotengine.org/ - open source powerful and flexible game engine.

https://www.blender.org/ - open source 3d creations suite.

https://www.reaper.fm/ - DAW used for soundtrack, paid license is required.

https://www.rolandcloud.com/ - useful set of virtual instruments to work on soundtrack, paid subscription is required.
