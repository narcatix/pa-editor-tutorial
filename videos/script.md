## §6 🛅 Prefabs (Older)
Prefabs allow for organisation and reusability of groups of objects. Prefabs are very useful—do not underestimate prefabs.
One important note—you cannot make prefabs containing other prefabs.
You can create a prefab by selecting one or more objectsin the timeline, hovering over the "Prefab" button on the control bar, and clicking the "Create" button. You will then be presented with these options in the prefab creation panel:
* Placement offset — Determines how far back from the scrubber will the prefab be placed on the timeline, in seconds
* Name — An arbitrary name of the prefab, allows for easier search from the prefabs list
* Description — An arbitrary description for your prefab
* Type — An arbitrary tag and colour coding for your prefab
When everything is set up, click the "Create prefab" button.

There are multiple levels to prefabs:
* The newly created prefabs are saved as a file in the folder of your editor—I will call those **prefab templates**.
* If you choose to spawn a prefab template into your level, the template will be used to create a **level prefab** which is stored within your level,
* and is immediately used to create a **prefab instance**, which is placed on the timeline.

You can spawn a prefab into the timeline by clicking "Prefab" button on the control bar, and then choosing a prefab from the list.
It may be confusing, but that list will always list **level prefabs** first, and **prefab templates** last. Choosing a prefab template will create a new level prefab and place an instance of it, while choosing a level prefab will only put an instance.

Prefab instance properties can be accessed by simply selecting a prefab instance in the timeline. Every instance can be modified to have a translation offset, and expanded into regular objects for modification. You can then collapse a prefab instance by selecting any object from that prefab on the timeline, scrolling down in the properties panel, and selecting either "Create New" for a new level prefab with the modifications applied, or "Apply to all" to update all instances of a **level prefab**.

You can also set up Quick Spawn for prefabs, which, once set up, allows you to spawn prefab instances with a press of one key (or a key-combination). That is very useful when trying to quickly spawn instances to the beat of music.
To set up quick spawn, click "Quick spawn config" in the prefab control bar menu.
You will be presented with a settings panel with 6 dropdown menus. Each one of them has these properties:
* Assign prefab under Prefab Assignment — opens a list of prefab instances and prefab template to choose from. That will be the prefab that will be spawned with a key.
* Active toggle under Keycode Assignment — toggles whether this Quick Spawn should listen to key presses.
* Assign key — after activating this button, press any key or hold multiple keys together that you want to use to quickly spawn a prefab instance.
You can have multiple Quick Spawns active at the same time.

You can delete a prefab instance object in the timeline and pressing delete. To delete a level prefab, use the "Delete" button in the prefab control bar menu, and choose the prefab you want to delete. Be careful, as the editor does not ask for confirmation, and deletion is permanent, unless you reload the level without saving, which may lose you some progress.
You cannot delete prefab templates from within the game, but you can delete them by deleting their file. You can quickly access the prefabs folder by using the "Create" button in the prefab control bar menu, and then clicking "Open Prefab Folder" in the prefab creation panel.

### Practice Example
- let's make this triangle into a prefab and spawn it periodically throughout a segment of the level.
- for that i will select the triangle object in the timeline and press the "create" button in the prefab control bar menu,
- in this prefab, i will leave the placement offset to be 0 seconds,
- name it "My first prefab",
- give it a description: "A very simple triangle attack that I made as my first prefab!",
- tag it... well, i guess "Bombs" describes it best...
- and then i will press the "Create Prefab" button.
- We now have a prefab of our triangle attack. I will now set up Quick Spawn for this prefab.
- I'll do that by pressing the "Quick Spawn Config" button in the prefab control bar menu,
- expanding the first Prefab Spawn,
- pressing "Assign Prefab" and choosing "My first prefab" from the list,
- pressing "Assign Key" and pressing any convenient for me keyboard button, in my case I'll set it to the Right Shift key, and then activating the "Active" toggle.
- I'll move the scrubber back to the beginning of this section, play the level, and start pressing the key I set in Quick Spawn config (Right Shift) whenever I want a prefab to appear.
- <<demonstration part of the last dash list item>>
- let's move the scrubber back again and see what we have now
- <<plays the level>>
- Let's say I want to change something about the attack, like make the rotation be random, and have it apply to every existing instance of this attack.
- For that I will expand a prefab instance by clicking on it on the timeline, then clicking on 'Expand Prefab Instance' in the properties panel.
- Now I can edit the triangle object to change its second rotation keyframe to be Linear random in range from 180° to 540°.
- After I'm satisfied with this change, I'll scroll down in the properties panel and press 'Apply to all' in the 'Prefab Collapse' section.
- Now if we replay the level, you can see all other instances have random rotation now.
- <<demonstration>>

## §7 😌 Break Time
<<video and audio fades in, with relaxing music, over the period of 10 seconds>>
<<the video should be a minute long>>

## §8 ⛓ Parenting (Older)
Parenting in Project Arrhythmia allows for objects to inherit different transformation components from another object, or the camera. Or, in simpler terms, parenting lets you "glue" one object to another, or to the camera.
Limitations of parenting include:
* An object can have only one parent, but any amount of children.
* An object can be a parent and a child at the same time.
* You cannot parent an object to a collapsed prefab instance.
* The maximum parenting chain limit is 15 objects.

You can parent an object by selecting the object you wish to be a child, then, in the properties panel, under the "Parenting" section, pressing one of the three buttons and choosing a parent:
* Magnifying glass — Opens a list of objects in the level to choose from
* Eye dropper — Lets you select an object from the timeline by simply clicking on it
* Camera — Immediately parents the object to the gameplay camera. Nothing to choose from here
Use any way that is convenient for you.

After a parent object has been chosen, you can modify what transformation components are inherited with three toggles under "Parenting" section:
* Position
* Rotation
* and Scale

It's a very advanced concept and you don't *have* to know this, but it's worth nothing, that:
- If a transformation component is enabled, the object will take that component from the parent object.
- If a transformation component is disabled, the object will try to look up the parenting chain to find an object with that component enabled, and take its parent's component. If it fails, it will assume default transformation for a component, which is (0; 0) for position, (1; 1) for scale, and (0) for rotation.
By default only Position and Rotation components are on. This is very important to keep in mind, sa you would want all 3 to be on in most cases.

Enabled transformation components give you an option to set up a time offset for those components. If there is an offset, the object will take the component from its parent with a time delay or prediction.

You can remove parenting from an object by either choosing a new parent, or pressing the red "X" button in the "Parenting" section.
You can also quickly jump to the parnt of any object (if one exists) by clicking on the name of the parent, or to any child of any object (if any exist) by clicking on the "children" button.

Remember the "Empy" object type mentioned in the Objects tutorial video? Those are used for parentings where the object only exists to hold transformation data for child objects. They are not drawn on the screen and are invisible, which makes them a bit more optimised for this use.

### Practice example
- Let's create a new attack — a crossbeam that appears at a random position on the screen with a warning.
- First I will create a new Empty object, and call it 'Crossbeam Master'. This object will be invisible and be the master-parent of our attack—it will control where our attack goes and its rotation.
- I will set its position to be randomised using the Linear option, and provide the ranges that cover the whole playing area. I can preview what the positions for the area edges are by turning on Grid under "View" in the menu bar, hovering over the edges with the cursor and checking the coordinate display.
- Now I will create a Helper object and call it 'Crossbeam Warning 1'. This object will act as a warning to players that highlighted area is about to hit them.
	- I will change its end time type to Fixed Time, and leave the end time to be 1 second, to give players enough time to react.
	- I will parent this object to 'Crossbeam Master' by scrolling down to the parenting section, clicking on the Eye Drop button, and then clicking on the 'Crossbeam Master' object on the timeline to choose it as a parent.
	- I can also do so by clicking the magnifying glass icon, looking for and clicking on an object called 'Crossbeam Master' in the list.
	- I'll make sure Scale parenting is on.
	- I will then change this object's Scale to be a very large number wise, for example 300 units, to make sure players never see the end no matter its position on the screen.
- So far we've got a beam warning that fades in at a random position on the screen and stays there for a second before disappearing.
-Let's duplicate this object. To do so, first select it on the timeline if it isn't already, and use the duplication keyboard shortcut with keys Ctrl and D.
- I will change the name of the duplicate to be 'Crossbeam Warning 2', and change its rotation to be 90°.
- Let's preview what we have got so far. I will also preview the randomisation by selecting the Crossbeam Master object and using the re-randomisation shortcut.
- Now I will create a new Normal object and call it 'Crossbeam Hit 1'. This object will hit players.
	- I will align the start time of this object to end time of Crossbeam Warning objects,
	- parent it to 'Crossbeam Master' in a convenient to me way, not forgetting to turn Scale parenting on,
	- and change its scale to match the scale of one of the warnings, which is 300 by 1 for me.
	- I will make this object last 0.5 seconds by changing its end time,
	- and duplicate it using the duplication shortcut, renaming it to 'Crossbeam Hit 2' and rotating the duplicate by 90°, just like how we did with the second warning object
- I can add a little bit of rotation randomisation to this attack by selecting 'Crossbeam Master', and changing its rotation keyframe to be liner random from -20 to 20. Now the entire attack looks like this.
- I can also create a new prefab out of this attacl.
	- Note that you have to select all objects that are in this attack. You can do that by either holding the Shift key and clicking on all the objects, or clicking and dragging on the timeline.
	- I will follow the usual process of creating a prefab, aligning Prefab Offset to be at the start of Crossbeam Hit objects.
	- I will name it 'Simple Crossbeam' and tag it with 'Beams'.
- I will place the prefabs throughout a segment of the lveel using Quick Spawn.
- Now this segment looks like this <<demonstration>>

## §9 ✨ Effects & Checkpoints (Older)
[[SCREENSHOT]]

Effects and Checkpoints is a special timeline tab that allows you to control the gameplay camera, full-screen effects, force player gravity, and level checkpoints. Everything except checkpoints is controller by keyframes and can be animated.
These keyframes control the camera:
* Move keyframes — control the current position of the gameplay camera, x 0 y 0 being the default.
* Zoom keyframes — control how far the camera is zoomed in. The range of values is between 2 and 80 units, with 30 being the default. Camera zoom is the amount of units between the centre of the camera and the top, so zoom of 30 units makes the gameplay area 60 units tall.
* Rotate keyframes — control the rotation of the camera. The range of values is between -180 and 180 degrees, with 0 being the default. The values are always absolute, so a keyframe with the value of 0 would return the camera to its normal position.
* Shake keyframes — make the camera shake around its current position with a set strength. The range of values is between 0 and 5, with 0 being the default.
These keyframes control fullscreen effects:
* Theme keyframes — control the current level theme, which defines colours used in the level. For instance colours of UI elements, gameplay object, parallax, and effects. Theme management and editing will be discussed in a later video.
* Chroma keyframes — control the strength of chromatic aberration. The range of values is between 0 and 8, with 0 being default.
* Bloom keyframes — control bloom intensity, diffusion, and colour.
	* Bloom Intensity — controls strength of the effect. The range is between 0 and 50, 0 being default.
	* Bloom Diffusion — controls how far the glow extends. The range is between 5 and 30, 7 being default.
	* Colour — controls the tint of glow. Takes a colour from 'Effects' palette in the current theme, or white, which is default.
* Vignette keyframes — control vignette intensity, smoothness, colour, whether vignette is round, and vignette centre position.
	* Intensity — controls how far the effect extends. The range is between 0 and 100, 0 being default.
	* Smoothness — controls how smooth the centre is. Negative values produce a weird result. The range is between -25 and 25, 0 being default.
	* Colour — controls what colour to use on the edges of the screen. Takes a colour from 'Effects' palette in the current theme, or black, which is default.
	* Force Round — controls whether the effect is screen ratio independent. A toggle that is off by default, meaning the effect depends on the screen ratio of the player.
	* Centre X and Y — control the centre position on the screen. Both ranges are normalised, with the value 0.5 being the centre or middle of the screen, which is also default.
* Lens keyframes — introduce an optical distortion effect.
	* Lens Distortion Intensity — controls how strong the ffect is. The range is between -80 and 80, 0 being default.
	* Centre X and Y — control the centre position on the screen. Both ranges are between -0.5 and 0.5, with 0 being the centre or middle of the screen, which is also default.
* Grian keyframes — add a film grain effect.
	* Grain Intensity — controls the opacity of the noise. The range is between 0 and 10, 0 being default.
	* Grain Size — controls the size of the overlayed noise texture. The range is between 0 and 9, being default.
	* Mix — whether to use a different blending mode. The range is from 0 to 1, but the different blending mode is only applied when the value is set to 1, which is also the default.
* Gradient keyframes — apply a fullscreen gradient.
	* Gradient Intensity — controls the strength of the effects. The range is between 0 and 2, 0 being default.
	* Gradient Rotation — controls the rotation of the gradient in hexacontades. The range is between 0 and 60, where 60 is a full rotation. 0 is the default.
	* Colours A and B — control what colours to use at the ends of the gradient. They take a colour from 'Effects' palette in the current theme, or white, which is default (but appears as black in the UI).
	* Overlay Mode — controls what blending mode to use and has 4 options: Linear, Additive, Multiply, and Screen. Linear is the default.
* Glitch keyframes — add a glitch-like effect.
	* Glitch Intensity — How much of the screen is covered in glitch strokes. The range is 0 to 1, 0 being default.
	* Glitch Speed — controls how often the effect refreshes. The range is 0 to 2, 1 being default.
* Hue keyframes — apply a fullscreen colour hue shifting effect. Measured in degrees. The range is 0 to 360.
Gameplay keyframes include:
* Player keyframes — are experimental and may change or be removed in the future. They force gravity on players. Takes two number values for Force X and Force Y measured in Unity Gravity units. Movement of 1 editor unit per second is equal to 33.333~ of Unity Gravity units.
* Checkpoints — are not exactly keyframes. They mark the time in level to which players return upon death after reaching this checkpoint and where the player spawn measured in editor units. Slider UI elements help you align the position relative to the current camera position.

## §10 🎨 Themes & §11 🏙 Parallax Objects (Older)
<<TODO: GAMEPLAY OBJECTS APPEAR AS IF THEY'RE ON PARALLAX DEPTH 69>>
[[SCREENSHOT]]
[[SCREENSHOT]]
[[SCREENSHOT]]
### Themes

### Parallax Objects
Parallax objects are a special type of objects that create a parallax effect when the camera moves. These objects do not appear on the timeline, and are very limited in functionality. There are 5 configurable layers for parallax objects, one of which can be selected as a Primary layer.
Current limitations of Parallax objects include:
* You can only animated them with limited Loop settings, and complex Events, no keyframes.
* Parallax objects are purely visual and do not affect gameplay,
* Parallax objects can only be selected for editing by clicking on them in the preview.
* Layer properties are static and cannot be changed throughout the level,
* Non-primary layers only allow you to choose one colour for all the parallax objects on that layer.

Parallax settings are accessible via "Settings" button in BG control bar popup. The settings panel has the following options:
* Primary Layer — that lets you choose which of the 5 layers (or none) will be counted as primary, letting you choose colours per-object on that layer,
* Depth of Field
	* Activation toggle, which is off by default,
	* and Value slider, which controls Depth of Field strength in range from 0 to 1000, 40 being default.
* 5 layer categories, each including:
	* Depth — slider controlling depth of the layer with values in range from 0 to 1000. Default values are 100 multiplied by layer number.
	* Colour — of all objects in the layer. Only available for non-primary layers. Takes a colour from 'Parallax' palette in the current theme.

Creation of new parallax objects is done through BG control bar popup. The Create button creates a new object on the first layer, while the buttons labeled 1 through 5 create a new object on the corresponding layer.

To edit a parallax object you must select it by clicking on it in the preivew. You will be presented with a Parallax Object panel which has the following options:
* under "General Settings":
	* Layer — 1 through 5.
	* Colour — Only available for objects on the primary layer. Takes a colour from 'Parallax' palette in the current theme.
	* Position X and Y — in editor units. Keep in mind thta Parallax layers are subject to foreshortening, so it might look like 1 editor unit is suddenly much smaller for that object.
	* Scale X and Y — in editor units.
	* Rotation — in degrees. The range is 0 to 360, and 0 is default.
	* Shape — Has categories on the top, and a list of shapes from the selected category below.
* and these options under "Animated Settings":
	* Active Animation Loops — group of 3 toggles for Position, Rotation, and Scale. Each activated toggle adds extra options below to define second as follows:
		* Position X and Y — in editor units. Marks the second position for animation loop.
		* Scale — in editor units. Sets the scale goal for animation loop.
		* Rotation — in degrees with values in range of 0 to 360. Sets the rotation goal for animation loop.
	* Loop Length — controls how long will transition between positions take, measured in seconds.
	* Loop Delay — which will make it so animation only starts when the provided time in the song is reached. Measured in seconds.

Deletion of parallax object is done by selecting the object and using the deletion shortcut.
Unfortunately, this is the only way to delete parallax objects at the moment.

Parallax objects have some Events associated with them that will be covered in a separate video in the series.

## §12 🎚 Miscellaneous Tools & Settings
[[SCREENSHOT]]
[[SCREENSHOT]]
[[SCREENSHOT]]

## §13 📤 Uploading & Updating Levels
[[SCREENSHOT]]

## §14 💨 Shortcuts
highest score! enter your name:

<<TODO: Keyframe value shortcuts—check Pidge's pins in the editor chat for the screenshot>>
<<TODO: Mention holding shift to select multiple objects>>

## §15 💡 Triggers & Events
highest score! enter your name:

## §16 💾 Scripts and File Editing
highest score! enter your name:

<<TODO: mention Parctan/QuadTools>>
<<TODO: mention backup files and how to restore backups>>

## §17 🛟 Tips For Better Level Design
higher score! enter your name:

<<TODO: also go over previously made attacks, adding style to them, explaining warning times, their styles, speed, and sync to music>>
	<<TODO: Bomb attack from Parenting and Prefabs have edge cases where you might see shrapnel not reach the end of the screen and disappear>>
<<TODO: mention different aspect ratios players may be playing on and how levels are affected>>
<<TODO: mention bitrate of level recordings and Grain effect>>
<<TODO: explain or link to a resource on basics of animation>>

## §18 🧐 Finished Level Overview (feat. _blank_)
highest score! enter your name:
<<stretch goal>>
<<TODO: Have a popular PA level creator go over one of their finished levels in the editor>>

## 🔨 Todo
<<TODO: UPdate prefab section with multi-object selection prefab updating>>
<<TODO: Update animation section with absolute rotation keyframes>>
<<TODO: Explain where to get music and how to convert it if needed>>
