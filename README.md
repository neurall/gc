# TerraVoxel ->  more voxel more Adidas

[67 Milion voxels Online Demo](https://neurall.github.io/terravoxel)
Viewable around 10M on mine crappy old notebook Intel Hd 3000 embeded GPU in (i5 cpu from 2011)

The aim of this project is to squeeze maximum number of cubes/voxels from HW.
Currently it uses  one voxel per triangle transparency trick and hw instancing.

Ie in the middle of every triangle is essentially quad with tris on sides by making tris transparent only quad part remains visible.
Advantage is that we can push twice as much faces as oposed to classic 2 triangle per quad on any hw.
The price we pay for this are depth sorting  zorder issues associated with transparency.

Since sorting milions of tris on cpu is not feasible one sollution is flipping meshes and its uv coordinates (TODO:)
every 180 camera angle thus preserving back to front rendering order (classic painters algo)
