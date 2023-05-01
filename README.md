# UE_BuildSystem
<a href="https://skillicons.dev"><img src="https://skillicons.dev/icons?i=unreal"/></a>

Made for unrealEngine 5.0<br>
This system allows the player to place, edit and delete blueprints in a level.


## Configuration

### Adding the Actor Component AC_BuildSystem:
In your player blueprint, add the component AC_BuildSystem by typing 'AC Build System'.<br>
![AddingAC](https://user-images.githubusercontent.com/38381564/235476707-ed426ef5-06e6-4bb0-980d-e1327bf4fc59.png)


### Action Mappings:
You will need to create 2 inputs: 

- BuildView (for exemple 'B')<br>
![BuildView](https://user-images.githubusercontent.com/38381564/235473652-40675de3-4082-4cd2-afa7-a93e6e827c12.png)
		

- PlaceBuildBlueprint (for exemple 'Left Mouse Button')<br>
![PlaceBuildBlueprint](https://user-images.githubusercontent.com/38381564/235473675-4f23c54c-c217-4fd5-8278-30ebb082b8a5.png)


### Player blueprint:
We need to define the references of the parent actor (player blueprint) and its camera.<br>
![playerBP](https://user-images.githubusercontent.com/38381564/235475613-c5b5fd52-9ee8-41e3-8c6f-398cebed8cc9.png)

Replace the player blueprint cast reference in the PC_BuildSystem with the one you put your AC_BuildSystem in:
![DefinePlayerCharacter](https://user-images.githubusercontent.com/38381564/235524539-39b97c75-60de-429b-bc5f-ce08410fe632.png)

## Settings

In the AC_BuildSystem, you can adjust some settings:

- SnapGridSize (This parameter is the distance between the points that make up the grid so that the object will snap to closest grid dot. By default, this value is 100,0.)<br>
![SnapGridSize](https://user-images.githubusercontent.com/38381564/235477530-51a30c6b-7325-4cc5-9508-2eed48c28ad6.png)

- HitDistance (This parameter corresponds to the maximum distance between the camera and where the player aims. By default, this value is 500,0.)<br>
This parameter is a local variable accessible from the BuildTrace function<br>
![BuildTracePath](https://user-images.githubusercontent.com/38381564/235479285-485b50b3-ca1c-4eaa-81ef-72428c458874.png)
![HitDistance](https://user-images.githubusercontent.com/38381564/235479305-9dec0bb2-cc0f-4067-8ddd-f20d770f031f.png)


