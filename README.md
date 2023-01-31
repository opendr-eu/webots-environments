# webots-environments

Custom Webots environments and controllers created in the context of the OpenDR European project.

# How to add a new environment
1. A subdirectory should should be created at the root level, and be given a meaningful name
2. The added project should follow Webots [standard file hierarchy](https://cyberbotics.com/doc/guide/the-standard-file-hierarchy-of-a-project#the-root-directory-of-a-project), namely it should contain:
- "controllers" folder: this directory contains the controllers used by the robots referenced by the world files of the current project.
- "protos" folder: this directory contains the local PROTO files referenced by the world files of the current project.
- "plugins" folder: this directory contains the physics plugins used by the current project.
- "worlds" folder: this directory contains the world files
3. All the necessary assets (images, custom PROTO files, meshes) should be included.

Note: if the controller requires additional data to be present (trained models, datasets, etc) to run, these should *not* be included.
The only requirement is that the world opens without warnings and/or missing assets.

Example:
```
├── hospital-environment
│   ├── controllers
│   │   ├── tiago_robot_controller.py
│   ├── worlds
│   │   ├── textures
│   │   │   ├── hospital_bed.png
│   │   ├── hospital_environment.wbt
│   ├── protos
│   │   ├── meshes
│   │   │   ├── gripper_mesh.stl
│   │   ├── textures
│   │   │   ├── gripper_texture.png
│   │   ├── CustomGripper.proto
```
