<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

### Bring Model Into Unreal

<sub>[previous](../) • [home](../README.md#user-content-ue4-animated-flag) • [next](../)</sub>

<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

Lets import the model into Unreal and set it up for being used as a skeletal mesh for the UE4 cloth system.

<br>

---


##### `Step 1.`\|`ITA`|:small_blue_diamond:

Open up the **Epic Games Launcher** and run the latest version of the game.

![epic games launcher](images/epicGamesLauncher.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 2.`\|`FHIU`|:small_blue_diamond: :small_blue_diamond: 

In the **Select or Create New Project** screen select a new **Games** project and press the <kbd>Next</kbd> button.  

The **Select Template** screen comes up and we will select **Blank** and press the <kbd>Next</kbd> button. 

![create a games project with the blank template](images/createNewProject.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 3.`\|`ITA`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

In **Project Settings** select a **Bluerprint** only project for **Desktop/Console** with no **Starter Content**.  Select a **Folder** and **Name** to store the new project.

![create new UE4 project with no starter content](images/createProject.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 4.`\|`ITA`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Create three new folders to hold assets needed for this walk through `Textures`, `Materials` and `StaticMeshes`.

![three folders to hold assets](images/create3Folders.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 5.`\|`ITA`| :small_orange_diamond:

Download the [T_USFlag.png](../Assets/T_USFlag.png) texture.  Drag and drop it into the **Textures** folder in the **UE4** project.

![import T_USFlag.png](images/usFlag.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 6.`\|`ITA`| :small_orange_diamond: :small_blue_diamond:

Now open up the **T_USFlag** texture.  Make sure it is a power of 2 size on both the **x** and **y** axis as well as a **Normal** compression with actual **Mip** levels.  Please note that the flag aspect ratio is distorted as we distored the UV's to be square.  When applied the aspect ratio should correct itself as the UV's will alter the textures aspect ratio to match the plane we created.

![flag texture has mips](images/FlagTexture.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 7.`\|`ITA`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

Create a new **Material** in the **Materials** folder and name it `M_Flag`.

![create m_flag material](images/newMaterial.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 8.`\|`ITA`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Open up **M_Flag** and right click on the empty graph.  Select a **Texture Sample** node.  Highlight the node and change the **Texture** to `T_USFlag`. Select the plane on the model preview panel.

![texture sample node and with t_usflag](images/textureSampleFlag.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 9.`\|`ITA`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Connect the **RGB** output pin from the **Texture Sample** node to the **Base Color** pin on the shader.

![rgb to base color connection](images/connectTexture.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 10.`\|`ITA`| :large_blue_diamond:

Add a **Constant** node and set it to `.45` and send it to the **Roughness** pin in the shader.  This will make the flag a bit shiny.  Lets leave it here for the material so lets press the <kbd>Apply</kbd> button.

![.45 to roughness](images/roughness.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 11.`\|`ITA`| :large_blue_diamond: :small_blue_diamond: 

Import **SK_Flag** that you crated in Maya and drag it into the **SkeletalMeshes** folder.  Select **Skeletal Mesh** and don't assign a skeleton.  In **Material Input Method** select `Do Not Create Material`.  Press the <kbd>Import</kbd> button.

![SK_Flag imported](images/importSKFlag.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>


##### `Step 12.`\|`ITA`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: 

*Double click* to open **SK_Flag** and assign the `M_Flag` to the **Material Slot**.

![M_Flag material assigned to SK_Flag](images/addMaterialToFlag.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 13.`\|`ITA`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

Now drag the **SK_Flag** into the game.  Notice that the flag lies flat and the pivot is on the wrong side.  Lets fix that.

![flag in game in wrong direction with bad pivot](images/badFlag.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 14.`\|`ITA`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

Open up **SK_Flag** in **Maya** and move the pivot to the opposite side by pressing **D** to adjust the location.

![pivot moved to other side of flag in maya](images/movePivot.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 15.`\|`ITA`| :large_blue_diamond: :small_orange_diamond: 

Move the pivot point to be in the `0, 0` location in the world.  It helps to see all four views to move it precisely to the center.

![move flag to center](images/movePivotToZero.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 16.`\|`ITA`| :large_blue_diamond: :small_orange_diamond:   :small_blue_diamond: 

Now select **File | Game Exporter** and the only major change we will make is select **Up Axis | Z**.  By default **Maya** is **Y** up and **UE4** is **Z** up.

![alt_text](images/zAxisExport.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 17.`\|`ITA`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

Go back to **Unreal** and delete the three files.  Re-import the new **SK_Flag** as a skeletal mesh with no material then press the <kbd>Import</kbd> button.

![reimported SK_Flag with skeletal mesh](images/reImportMaterail.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 18.`\|`ITA`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Open up the new **SK_Flag**.  Assign the **M_Flag** to the skeletal mesh.  Save the work and drag **SK_Mesh** into the level.  Now the orientation is correct and the pivot point is on the right side.

![material assigned to sk_flag and is in game scene](images/assginMFlagReimport.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 19.`\|`ITA`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Lets add a **Basic | Cylinder** to the level and call it `Flag Pole`.  Change the **Transform | Scale** to `0.1, 0.1, 3.0`.  Position it in the middle of the level.

![add cylinder as flagpole in the scene](images/addFlagpole.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 20.`\|`ITA`| :large_blue_diamond: :large_blue_diamond:

1.  Adjust the flag to be on the right part of the pole.  Look at it from all angles.

2.  Adjust the **Player Start** to be in front of the flag. Rotate it so the **X** axis faces the flag.

3.  When you hit play you should see the flag.

![adjust flag, player start to face flag pole](images/setUpPole.png)


<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 21.`\|`ITA`| :large_blue_diamond: :large_blue_diamond: :small_blue_diamond:

Add a folder called **Maps**. Press **File | Save Current** and save the room and call it `FlagMap`.

Open up **Project Settings** and select **Maps and Modes**.  Change the default room at load to **FlagMap**.

![save room and make default](images/nameRoom.png)


___


<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

<img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=Next Up - ADD NEXT TITLE">

<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

| [previous](../)| [home](../README.md#user-content-ue4-animated-flag) | [next](../)|
|---|---|---|
