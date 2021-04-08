# PlanetWalker
Simple game to learn Godot engine and 3d modeling techniques along with producing synth soundtrack for games. Gamer will control rover to find crystals on planet surface. Be ready to accept challenge splitted by many levels.

## Why voxel art?
Easy to create, fun to work and beatiful to look. But for me personally voxel art is a way to transform pixel art experience from 90-s to modern 3D world.

## Game concept - levels
Planet Walker game consists of multiple levels which a quadrants connected to each other via entrance systems or not. Should be possible to quickly define new maps as matrix with octet types and connect to each other.

## Game concept - gameplay
User drives rover on planet via remote control from orbital station, finds new paths and important artefacts and objects. 

Point of interests for player:
1. Usage of radio tranceiver for rover control - select satellite placed at orbit around planet, select frequency, enter pin code, list with error codes received from rover, specific command to rover (sleep, reboot to reset errors, activate, ping etc).
2. Charge level of batteries - low usage in sleep mode, while radio, electro engines, camera and light require much more energy. Search for landed charging stations.
3. Coordinates usage - rover can define location where it placed if at least 3 connection satellites available on orbit and rover has connection with them.

## Mesh libraries in Godot
Mesh libraries is core technique in this game which make possible to quickly and easily generate levels from prepared set of meshes. Usage of MeshLibrary object in Godot is not really trivial but is not rocket science same time. You need to keep in mind 3 important points:
1. To export scene as mesh library you should create new scene from nowhere (Scene->New Scene), such scene must not have any root scene or root nodes. Although it is ok to save such scene to separate tscn file.
2. Avoid creation of separate material for your object along with mesh - such material will not be exported to MeshLibrary and you will get mesh without texture, instead of that add material to mesh directly (Inspector -> Mesh -> Edit -> Surface 1 -> Material).
3. And finally to create new MeshLibrary: Scene -> Convert to... -> Mesh library, in dialog enter name of file with MeshLibrary, don't forget to enter meshlib extension or you will get error.

To use prepared set of meshes you need to add GridMap to your scene and choose MeshLibrary for it (also work to drag meshlib file from FileSystem tab to MeshLibrary property of GridMap object).

Use WASD keys to rotate tiles while adding them from MeshLibrary to scene.

## Preparation of 3D models
Working with models including 3 steps:
1. Create voxel art model in MagicaVoxel editor.
2. Export voxel art model to wavefront format (obj file with png as texture palette).
3. Import wavefront file to Blender, save blender project, geometry gets optimized here.
4. Export blender model to wavefront file, save it to models folder of godot project. 3D model is ready to use.

## Toolset
https://www.voxelmade.com/magicavoxel/ - opens ource very useful tool to create voxel models.

https://godotengine.org/ - open source powerful and flexible game engine.

https://www.blender.org/ - open source 3d creations suite.

https://www.reaper.fm/ - DAW used for soundtrack, paid license is required.

https://www.rolandcloud.com/ - useful set of virtual instruments to work on soundtrack, paid subscription is required.

https://www.pixilart.com/ - pixel-art community and drawing tool.
