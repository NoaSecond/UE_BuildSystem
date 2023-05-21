# UE_BuildSystem
<a href="https://skillicons.dev"><img src="https://skillicons.dev/icons?i=unreal"/></a>

Made for unrealEngine 5.0<br>
This system allows the player to place, edit and delete blueprints in a level.

# Table of contents:
1. [Configuration](#configuration)<br>
1.2. [Inputs](#inputs)<br>
1.2.1. [Action mappings](#action-mappings)<br>
1.2.2. [Axis mappings](#axis-mappings)<br>
1.3. [Create placeable blueprint](#create-placeable-blueprint)<br>
1.4. [Create a new terrain](#create-a-new-terrain)<br>

2. [Settings](#settings)<br>
2.1. [SnapGridSize](#snapgridsize)<br>
2.2. [BuildHitDistance](#buildhitdistance)<br>
2.3. [DeleteHitDistance](#deletehitdistance)<br>
2.4. [RotationSensivity](#rotationsensivity)<br>

## Configuration

### Inputs
You will need to create 6 action mappings and 1 axis mapping : 

#### Action mappings

- Delete
This action is used to delete a placeable blueprint.<br>
By default 'Right Mouse Button'.<br>

- PlaceBuildBlueprint
This action is used to place a placeable blueprint.<br>
By default 'Left Mouse Button'.<br>

- DeleteMode
This action is used to switch to the deletion mode.<br>
By default the key 'V'.<br>

- Unload
This action is used to unload the selected placeable blueprint.<br>
By default the key 'U'.<br>

- Jump
This action is used to jump.<br>
By default the key 'Space Bar'<br>

- ToggleMouseCursor
This action is used to show or hide the mouse cursor and acces to the HUD menu.<br>
By default the key 'I'.<br>

#### Axis mappings

- Fly Up / Down
This axis is used to fly up or down during fly only.<br>
By default, scale 1 (UP) is 'Space Bar' and scale -1 (DOWN) is 'Left Ctrl'<br>


### Create placeable blueprint
To add a new placeable blueprint, right-click on BP_PlaceableBlueprint and click on 'Create Child Blueprint Class'.<br>
For each created component, add it to the table by creating a new row in the DT_BS_PBList DataTable.<br>


### Create a new terrain
To add a new terrain, right-click and add a new 'level' in the folder named 'Terrains'.<br>
Open the level and set in 'World Settings' the option 'GameMode Override' to 'GM_BuildSystem'.<br>




## Settings

### SnapGridSize
This parameter is the distance between the points that make up the grid so that the object will snap to closest grid dot.<br>
By default, this value is ```100,0```.<br>

### BuildHitDistance
This parameter corresponds to the maximum distance between the camera and where the player aims when he is in the build mode.<br>
By default, this value is ```5000,0```.<br>
This parameter is a local variable accessible from the BuildTrace function.<br>

### DeleteHitDistance
This parameter corresponds to the maximum distance between the camera and where the player aims when he is in the delete mode.<br>
By default, this value is ```500,0```.<br>
This parameter is a local variable accessible from the BuildTrace function.<br>

### RotationSensivity
This parameter corresponds to the degree of rotation added to each scroll.<br>
By default, this value is ```45,0```.<br>