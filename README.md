# 📄 Paper Engine

Paper Engine is an extension for GDevelop that simulates a 3D environment allowing you to use 2D sprites to create planes

#### ❗ The Paper Engine does not work with Gdevelop's built-in 3D ❗

## Getting Started

### Download and Install

You can [download the extension by clicking here](https://raw.githubusercontent.com/FlokiTV/Paper-Engine/main/PaperEngine.json). 

To load the extension in gdevelop :
 1. access the menu
 2. click on "create a new or search for new extensions"
 3. click on "load extension"
 4. select the extension "PaperEngine.json"

![how to install](https://i.imgur.com/OzQMsuI.gif)

## Before Starting

### Environment

The environment in the paper engine is not 3D. The technique used to simulate the environment is just changes in scale and skew of objects.
Automatically the entire scene is scaled in half to give the feel of an isometric map. There are two types of objects, **tiles** and **planes** by default

##### All extension objects are positioned based on the values of the X, Y and Z variables

#### Tiles
Tiles are 2D objects, but they have the Z property so they can have an elevation of the ground. The tiles follow the same scale as the scene to give the feeling that they are in the same direction as the ground.

The point of origin of the tile is at the **center**

#### Planes
Projecting a sprite will make it scale normalized and behave like a wall. As you rotate the camera angle, it will distort to maintain the wall angle.

When set to follow the camera angle, your projected sprite will always face the camera. Useful for creating characters with the "billboard" effect.

The point of origin of the plane is at the **center bottom**

#### Collisions 
By changing the scale and skew of the object and rotating the camera, we lose the object's 2D collision from the initial position.

To get around this, we can create a separate object just to be the collision and put at the bottom of the walls