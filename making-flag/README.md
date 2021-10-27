<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

### Making a Flag

<sub>[previous](../) • [home](../README.md#user-content-ue4-animated-flag) • [next](../)</sub>

<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

Lets go into Maya and create a flag that we will import into Unreal.

<br>

---


##### `Step 1.`\|`ITA`|:small_blue_diamond:

Open up **Maya 22** to create a new plane to hold our flag. 

![open up Maya 22](images/openUpMaya.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 2.`\|`FHIU`|:small_blue_diamond: :small_blue_diamond: 

Make sure you are on the **Poly Modeling** tab and drag a plane into the scene.  Since the flag is essentially flat we will use a flat plane.

![drag plane into the scene](images/dragPlane.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 3.`\|`ITA`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

We need to make sure that the units match Unreal's default units.  So 1 **Maya** unit needs to be in **cm**.  So go to **Windows | Settings/Preferences | Preferences | Settings** and make sure **Working Units | Linear** is set to `centimeter` and **Angular** is set to `degrees`. Press the <kbd>Save</kbd> button.

![change linear working units to centimeters](images/setUnitCM.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 4.`\|`ITA`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

A common size for the **[US Flag](https://en.wikipedia.org/wiki/Flag_of_the_United_States)** is 3' by 5'.  If we convert this to centimeters it is 91.44cm to 152.4cm.

![flag size of 3' by 5'](images/sizeOfFlag.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 5.`\|`ITA`| :small_orange_diamond:

Select the **Outliner** and make sure you have the **pPlane1** selected.  Change the **Width** to `152.4` and the **Height** to `91.44`.  Also, a flag is rarely flat on the ground so lets put it upright (like it is on a flag pole) by rotating the **Rotate X** axis by `90` degrees.

![alt_text](images/changeScaleAndRotation.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 6.`\|`ITA`| :small_orange_diamond: :small_blue_diamond:

Now animation happens on the vertices.  So the more vertices the more folds and realistic animation we will get.  Now this comes at a cost to performance.  Lets pick a pretty dense mesh to see how good it can look. Lets set the **Subdivision Width** to `60` units.  Now for a 3 x 5 aspect ratio model, to make these subdivisions square we need to find out the height.

Divide height by width or 3/5 or 0.6.  Now multiply 60 by .6 which equals 36. So lets set the **Subdivision Height** to `36`.

![set subdivision width and height to 60 and 36 respectively](images/subD.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 7.`\|`ITA`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

Open up the **UV** editor window to look at our UV's.

![open up UV Editor in Maya](images/openUpUVEditor.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 8.`\|`ITA`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now the UV's are not taking the entire height and show a gap. 

![show gap in uv](images/UVGap.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 9.`\|`ITA`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Click no the **vertex selection** tool and drag the mouse around all the vertices to select them.  Change to the scale tool and scale it on the **V** axis.  It needs to scale by .4 units (4 grids).

![scale UV's by .4 units on y](images/UVEdtior.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 10.`\|`ITA`| :large_blue_diamond:

Change to the transform tool. Move the UV set to fit with the `0` and `1` range.  I had to move it up .2 units on the **v** axis.

![center uv's in zero to one](images/moveUVtoZeroOne.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 11.`\|`ITA`| :large_blue_diamond: :small_blue_diamond: 

Press the <kbd>D</kbd> key and move the pivot point to the left center of the object.  This is where it would get attached to a flag pole.  Zoom in and make sure it is bound to the middle edge vertice.

![move pivor point to center left of flag](images/pressDCenterPivot.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>


##### `Step 12.`\|`ITA`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: 

![alt_text](imagescleanFile/.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 13.`\|`ITA`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

![alt_text](images/.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 14.`\|`ITA`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

![alt_text](images/.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 15.`\|`ITA`| :large_blue_diamond: :small_orange_diamond: 

![alt_text](images/.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 16.`\|`ITA`| :large_blue_diamond: :small_orange_diamond:   :small_blue_diamond: 

![alt_text](images/.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 17.`\|`ITA`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 18.`\|`ITA`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 19.`\|`ITA`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 20.`\|`ITA`| :large_blue_diamond: :large_blue_diamond:

![alt_text](images/.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 21.`\|`ITA`| :large_blue_diamond: :large_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

___


<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

<img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=Next Up - ADD NEXT TITLE">

<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

| [previous](../)| [home](../README.md#user-content-ue4-animated-flag) | [next](../)|
|---|---|---|
