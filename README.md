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
2.2. [RotationSensivity](#rotationsensivity)<br>
2.3. [BuildHitDistance](#buildhitdistance)<br>
2.4. [DeleteHitDistance](#deletehitdistance)<br>

## Configuration

### Inputs
You will need to create 6 action mappings and 1 axis mapping : 

#### Action mappings

- Delete
This action is used to delete a placeable blueprint.<br>
By default 'Right Mouse Button'.<br>
![Delete](https://github.com/YoruKiwi/UE_BuildSystem/assets/38381564/f47fc9cd-ad74-4cda-bfe7-9fb11cb13d67)<br>


- PlaceBuildBlueprint
This action is used to place a placeable blueprint.<br>
By default 'Left Mouse Button'.<br>
![PlaceBuildBlueprint](https://github.com/YoruKiwi/UE_BuildSystem/assets/38381564/f35d167f-2c2b-427e-9855-72a49ea356f5)<br>


- DeleteMode
This action is used to switch to the deletion mode.<br>
By default the key 'V'.<br>
![DeleteMode](https://github.com/YoruKiwi/UE_BuildSystem/assets/38381564/98063e06-8df0-44af-94a5-4ea9dce48c0b)<br>


- Unload
This action is used to unload the selected placeable blueprint.<br>
By default the key 'U'.<br>
![Unload](https://github.com/YoruKiwi/UE_BuildSystem/assets/38381564/1b8f5fc7-55fc-4b08-8ceb-4aba848f379a)<br>


- Jump
This action is used to jump.<br>
By default the key 'Space Bar'<br>
![Jump](https://github.com/YoruKiwi/UE_BuildSystem/assets/38381564/67993762-a4a9-4a00-8c49-8a1e9580bcc7)<br>


- ToggleMouseCursor
This action is used to show or hide the mouse cursor and acces the HUD menu.<br>
By default the key 'I'.<br>
![ToggleMouseCursor](https://github.com/YoruKiwi/UE_BuildSystem/assets/38381564/2ad5f94f-04fa-4a57-af79-1d271361370a)<br>


#### Axis mappings

- Fly Up / Down
This axis is used to fly up or down during fly only.<br>
By default, scale 1 (UP) is 'Space Bar' and scale -1 (DOWN) is 'Left Ctrl'<br>
![Fly_Up_Down](https://github.com/YoruKiwi/UE_BuildSystem/assets/38381564/57044f44-d183-4121-89c8-cd7e4b1db0d0)<br>



### Create placeable blueprint
To add a new placeable blueprint, in the folder 'PlaceableBlueprint' right-click on 'BP_PlaceableBlueprint' and click on 'Create Child Blueprint Class'.<br>
![BP_PlaceableBlueprint](https://github.com/YoruKiwi/UE_BuildSystem/assets/38381564/5270957d-ca0f-43f0-871d-8783dac7b18f)<br>
![CreateChild](https://github.com/YoruKiwi/UE_BuildSystem/assets/38381564/ab23c992-761f-471d-8f11-cca280757f99)<br>
For each created component, add it to the table by creating a new row in the 'DT_BS_PBList DataTable'.<br>
![DT_BS_PBList](https://github.com/YoruKiwi/UE_BuildSystem/assets/38381564/d2b64064-8d65-4135-8985-02f4fdcc9314)<br>


### Create a new terrain
To add a new terrain, right-click and add a new 'level' in the folder named 'Terrains'.<br>
Open the level and set in 'World Settings' the option 'GameMode Override' to 'GM_BuildSystem'.<br>
![GameMode_Override](https://github.com/YoruKiwi/UE_BuildSystem/assets/38381564/f90c7971-5445-43e5-916e-7c46e5615573)<br>




## Settings

### SnapGridSize
This parameter is the distance between the points that make up the grid so that the object will snap to the closest grid dot.<br>
By default, this value is ```100,0```.<br>
![SnapGridSize](https://github.com/YoruKiwi/UE_BuildSystem/assets/38381564/9edab2a4-62e1-46fb-adf7-ebe65ef047db)<br>

### RotationSensivity
This parameter corresponds to the degree of rotation added to each scroll.<br>
By default, this value is ```45,0```.<br>
![RotationSensivity](https://github.com/YoruKiwi/UE_BuildSystem/assets/38381564/a63e3499-ae2a-4d3f-b2bf-86e2face9fe0)<br>

### BuildHitDistance
This parameter corresponds to the maximum distance between the camera and where the player aims when he is in the build mode.<br>
By default, this value is ```5000,0```.<br>
This parameter is a local variable accessible from the BuildTrace function.<br>
![BuildHitDistance](https://github.com/YoruKiwi/UE_BuildSystem/assets/38381564/269ce7bd-935c-4795-8ff8-b8a21ed8cfc3)<br>

### DeleteHitDistance
This parameter corresponds to the maximum distance between the camera and where the player aims when he is in the delete mode.<br>
By default, this value is ```500,0```.<br>
This parameter is a local variable accessible from the BuildTrace function.<br>
![DeleteHitDistance](https://github.com/YoruKiwi/UE_BuildSystem/assets/38381564/0f0b5f44-3151-47d9-a24f-901f1d17c408)<br>
