# UE_BuildSystem
<a href="https://skillicons.dev"><img src="https://skillicons.dev/icons?i=unreal"/></a>

Made for unrealEngine 5.0<br>
This system allows the player to place, edit and delete blueprints in a level.

# Table of contents:
1.[Configuration](#configuration)<br>
1.1.[AC_BuildSystem](#ac_buildsystem)<br>
1.2.[Player blueprint reference](#player-blueprint-reference)<br>
1.2.[Action Mappings](#action-mappings)<br>
1.2.[Create placeable blueprint](#create-placeable-blueprint)<br>

2.[Settings](#settings)<br>
1.2.[SnapGridSize](#snapgridsize)<br>
1.2.[HitDistance](#hitdistance)<br>

## Configuration

### AC_BuildSystem
In your player blueprint, add the component AC_BuildSystem by typing 'AC Build System'.<br>
![AddingAC](https://user-images.githubusercontent.com/38381564/235476707-ed426ef5-06e6-4bb0-980d-e1327bf4fc59.png)

### Player blueprint reference
In the PC_BuildSystem, redefine the reference to the player's blueprint and camera. (The camera reference will allow to place a blueprint where the player looks)<br>
![DefinePlayerCharacter Camera](https://user-images.githubusercontent.com/38381564/235527330-0339120f-c158-4fce-ac53-47b75cc7bb8d.png)


### Action Mappings
You will need to create 2 inputs: 

- BuildView (for exemple 'B')<br>
![BuildView](https://user-images.githubusercontent.com/38381564/235473652-40675de3-4082-4cd2-afa7-a93e6e827c12.png)
		

- PlaceBuildBlueprint (for exemple 'Left Mouse Button')<br>
![PlaceBuildBlueprint](https://user-images.githubusercontent.com/38381564/235473675-4f23c54c-c217-4fd5-8278-30ebb082b8a5.png)

### Create placeable blueprint
To add a new placeable blueprint, right-click on BP_PlaceableBlueprint and click on 'Create Child Blueprint Class'.<br>
![PlaceableBlueprint](https://user-images.githubusercontent.com/38381564/235532845-e03df69a-31d9-4b72-8ac2-99a06a71d924.png)<br>
![CreateChild](https://user-images.githubusercontent.com/38381564/235532860-b3ed14d8-e701-41a7-b61b-35e0659032a2.png)<br>

For each created component, add it to the table by creating a new row in the DT_BS_PBList DataTable.<br>
![RegisterNewPB](https://user-images.githubusercontent.com/38381564/235532325-55d2f2fd-b73a-43be-8615-3f208db3fd53.png)


## Settings

### SnapGridSize
This parameter is the distance between the points that make up the grid so that the object will snap to closest grid dot. By default, this value is 100,0.<br>
![SnapGridSize](https://user-images.githubusercontent.com/38381564/235477530-51a30c6b-7325-4cc5-9508-2eed48c28ad6.png)

### HitDistance
This parameter corresponds to the maximum distance between the camera and where the player aims. By default, this value is 500,0.<br>
This parameter is a local variable accessible from the BuildTrace function<br>
![BuildTracePath](https://user-images.githubusercontent.com/38381564/235479285-485b50b3-ca1c-4eaa-81ef-72428c458874.png)<br>
![HitDistance](https://user-images.githubusercontent.com/38381564/235479305-9dec0bb2-cc0f-4067-8ddd-f20d770f031f.png)


