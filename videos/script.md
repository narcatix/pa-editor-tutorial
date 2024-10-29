## §1 👋 Introduction
> *Montage of some cool Project Arrhythmia levels*

This is Project Arrhythmia. A fun rhythm bullet-hell game in which all things beautiful are deadly. The game has a broad library of thousands of challenging, beautiful, and creative levels made by members of its community.
> *The montage zooms out to show the levels are being previewed in the editor*

One of the appealing features of this game is its robust level editor used to create all of these levels.

Whether you're a new or a returning creator and you want to learn how to make a Project Arrhythmia level like *this*, or *this*, or *this*, then you're in the right place.
> *Recording of a level that will be created and finished in the tutorial*

In this tutorial I will explain the basics, walk you through creating this simple level you see on the screen, and by the end you will have enough knowledge to start making and publishing your own creative levels.

In every video there are useful links and update notes in the description, and the videos have captions available.

Now, forget about N-Chan. Today *I* am your guide to the Project Arrhythmia editor...

## §2 🚧 Making a New Project
![(Level creation screen screenshot)](assets/welcome-create-level.png)<br>
##### Song
First things first, we need to choose what song to use for our level. For new creators I recommend going with something fairly short and simple at first.

One important thing to note is that if you're planning to publish your level, make sure the song you're going to use is verified for Project Arrhythmia, otherwise it will be removed by moderators after being published. I will link information about this in the description.

In this tutorial I will use [Sphero by Xtrullor](https://www.newgrounds.com/audio/listen/612751) which is verified and free to download. I linked the download page in the description.

##### Create
To start creating we will need to make a new project. Open up the editor by selecting "Creation engine" in the main menu, then switch to the "Create level" tab on the sidebar.

You will be asked to fill in a few fields with information about the song and your level. Make sure to get them right, otherwise the song artist will be upset, and we don't upset artists in Project Arrhythmia.
* I will give this level a title, which will be "My first level". This can be anything you want to call it.
* For **Song Title**—since I'm using Sphero made by Xtrullor—I'll put "Sphero", because that is the title of the song, obviously.
* The **Song Artist** is "Xtrullor".
* Audio file location — here you click Browse and choose the song file. Sphero.mp3. Now, you *can* use files of .ogg, .mp3, and .wav audio formats, but they will all be transcoded into .ogg at the end of the day. Also do note that the editor is a bit quirky with some .mp3 files and might not create the project properly, in which case you'll have to use a different file format.
* Level artwork — this is where you select a level icon. The icon should be a .jpg image no bigger than 512 pixels squared. I will leave it blank for now, you can always set it later.
* Level background setup lets you create a level with a preset of backgrounds which are purely visual. I will select "City" because I think it's pretty.

Click the "Create new level" button, a new empty project is created, let's pause the playback... and welcome to the editor.

## §3 🖼 Overview
![(Editor interface overview)](assets/overview.png)<br>
##### Editor Interface
Now that we have a project loaded, let's take a look at the main interface of the editor. It is divided into multiple distinct windows.

##### Level Preview
So, this big view on the top-left is the **Level Preview**. This is where you can see how your level looks at any given time and this is what the players will see when playing your level. Now, you can control the current time of the preview by dragging around the blue handle at the bottom like this.

I'll drag it all the way to the very beginning and you can see there is a red square shape moving around on the preview while I'm doing that. That is a gameplay object. I can click on its shape to select it.

##### Property Editor
Now, what if I wanted this shape to be a circle? I can do that by using the **Property Editor** window to the right of our Level Preview. This window is different depending on what you have currently selected. If I select any of the dark squares—which are background or "parallax" objects, by the way—the property window will show properties specifically for parallax objects.

So if I want to change the shape of the gameplay object I will select it, go over to the "Shape / Gradient" section, and click on one of the 6 shape categories, for example, a circle.

Some properties like position, scale, rotation, and colour have their own animation timeline which is shown at the bottom of this window, which we will get back to in a minute.

By the way, don't worry about all the other properties yet. In this video I'm only going over the main interface of the editor.

##### Timeline
Next thing I'm gonna show you is the **Timeline** that spans the entire bottom half of the editor. The timeline is where we can see the representation of all the gameplay objects in the level placed at specific points in time, which we only have one of right now. I can click on an object in this window and that will select it just like clicking on its shapes in the Level Preview did.

If I click play on the Control Bar you will see the blue handle starts moving to the right, indicating that the time is advancing. We call this blue handle a "Scrubber". By the way, the shortcut to play or pause the level is Spacebar.

The length of the objects on the timeline represents how long they appear on the screen for. If the scrubber is on top of an object, that means that object exists at the current time. I can change the time an object appears by dragging it around the timeline.
I can hold shift while dragging to move an object up and down, but it doesn't change anything about the actual level, just makes it easier to organise your objects later on.

##### Property Editor (Keyframes)
Now, let's come back to the four special properties of gameplay objects. Did you notice that our object has an animation where it slowly moves to the right? So why is that? If I select the object and look at its animation timeline... aaAAaah... There we have a line labelled "Move" with two funny diamond shapes on it. These diamonds are what we call "Keyframes" and they define specific values to transition between.

As you can see, there are two "move" keyframes. I can click on one to start editing its values in the top-right portion of the window. The first keyframe defines position X 0 Y 0, which is the middle centre, and the second keyframe defines position X 10 Y 0, which is just to the right of that. Let's edit its position to be X 10 Y 10 and play the level. As you can see, the object is now moving diagonally from the centre.

Just so you know, Project Arrhythmia coordinates have X positive going right and Y positive going up.

I can zoom in and out both of the timelines using the shortcuts Ctrl+\[+\] and Ctrl+\[-\], create new keyframes by clicking with the right mouse button on an empty space, and delete keyframes by having them selected and using the Delete key.

Another fun way to create a new keyframe is clicking and dragging the object around right in the level preview! That will immediately create a new keyframe at the position of the scrubber, or update it if there is one already.

There are 4 dragging modes that can be used with 4 keyboard keys: W for position mode, E for scale mode, R for rotation mode, and T for colour mode.

##### Control Bar
So now you know how to work with one gameplay object, but there's only so much you can do with just that, so let's create another one. For that I will use the **Control Bar** which is situated right below the Preview Window. The Control Bar lets you do things like control playback, change the timeline layer, and create new objects. So to create a new object I simply click on the button that says "Object", and here it is, in the middle-centre of the preview. It's so small, let's make it bigger by changing the drag mode to "size" with E, and dragging from it in the preview.

If I want to delete an object I would select it either by clicking on it on the timeline or on its shape in the preview, and using the Delete key.

##### Menu Bar
Let's say I want to save my project. For that I would use the **Menu Bar** at the very top of the editor. I click "File" and then "Save Level", or simply use the Ctrl+S shortcut. You can see the list of other useful shortcuts under "Help", "Key Shortcuts".

It is important to remember to save your progress often, as Project Arrhythmia is still in Early Access and has some bugs that could cause crashes.
The game also saves a backup of your level periodically, and those will be discussed in [§16 💾 Scripts and File Editing](#16--scripts-and-file-editing).

When it is time to come back to working on a level after a nice break, you can always open the level project from the welcome screen by finding it in "Recent Levels" section in the "Home" tab, or in the "Open level" tab.

##### Getting Help
Lastly, I just want to say that if you find any of this very difficult—don't worry. Level creation has a bit of a learning curve and you're right at the beginning, so if you keep going, you will quickly get over the initial struggle. You can also ask for help in the comments, Steam Discussion forums, or in the official Project Arrhythmia Discord server, people will gladly help you there.

## §4 📦 Objects
Objects are the most essential part of the gameplay and decorations of a level. They appear as a shape and an be animated.

I'll create a new object by clicking on the "Object" button on the control bar. I can also create one from the presets if I use the Object control bar popup.
As you can see I now have an object placed on the timeline, represented by a rectangle. Its horizontal position indicates when the object starts and stops, which means that if I move the blue timeline scrubber to overlap with the rectangle you'll se it on the preview. I can click and drag the rectangle around the timeline and it will change its start time.

If I want to edit the object (i.e. change its shape, when it starts and ends, its transformation and colour) I'd have to select it by either clicking on it on the timeline, or in the preview. When I have an object selected you'll see the Object Properties panel show up to the right of the preview
Objects have these properties that I can edit:
* Name — A name, which is just to help me keep track of the object on the timeline. I can call this one 'Hello PA', and you will see this object's name update there.
* Colour coding — Six toggles that also help identify objects on the timeline by changing how they appear there. Having multiple of them toggled will mix the colour. I can toggle the Blue and Red empty toggles and you will see the rectangle on the timeline is now purple.
* Object Type — You can choose from
	* Hit — The object will hit players on collision, if fully opaque. It is used for obstacles.
	* No hit — The object will never hit players. It is used for decorations.
	* and empty — The object will be invisible. It is used for parenting, which will be discussed in a later video.
Next property is
* Start Time — Lets me control when the object appears and starts animating, measured in seconds relative to song start. It's the same as moving the object around on th etimeline, but you can set a precise time here.
* End Time — Tells the game when the object is no longer needed, making the object disappear and helping reduce lag. It has the following options:
	* Last Keyframe — The object will disappear immediately as its last animation keyframe is reached. Animation will be discussed in a separate video.
	* Last Keyframe + Offset — The object will disappear when the provided amount of time in seconds has passed after its last keyframe. So if this object's animation lasts 5 seconds, and the End Time is set to be Last Keyframe + Offset with the value 3, then the object will disappear 9 seconds after Start Time.
	* Fixed Time — Disappears the specified number of seconds after the object's Start Time.
	* Song Time — Disappears the specified number of seconds after the start of the song.
Next property is
* Parenting, which will have its own video in the series
* Gradient — Lets me set the gradient type or disable it for this object. There are 5 options: No gradient, Linear, Linear inverse, Radial, and Radial inverse. If a gradient is selected, colour keyframes for this object will ask for two colours to be chosen instead of one.
* Shape — Lets me set the shape of th object. It has categories on the top, and a list of shapes from the selected category below. I can click on the circle category and then choose a semmi-circle shape and you will se the shape on the preview update to be a semi-circle.
* Render Depth — Determines if the object is behind or in front of other objects. Lower values make the object go on top of other objects. If I were to have multiple objects overlapping on top of each other, where the first object is at depth 15, then setting the second object's depth to 14 would make it appear on top, while setting it to 16 would make it appear behind.
* Origin Point — Determines where the centre of the shape is, I can set it to be on the top-right of the shape, rather than its centre.
* and lastly, Keyframes timeline — Defines position, scale rotation, and colour properties of the object and allows for animation of those properties. When you create a new object, it has 1 initial keyframe for every line on the timeline, at the very beginning. You can't move or delete these initial keyframes. Animation will be discussed in a future lesson.

Having so many properties may seem overwhelming at first, but I'm sure you will have no trouble navigating through them with a bit of practice!

If I want to delete an object, I can do that by selecting it, and either clicking the little bin icon in the properties panel, or pressing the delete key on my keyboard. You will see the Object Properties panel close and the object disappear both from the timeline and preview.

### Practice example
Now let's have a practice example! During practice examples I will be showing you how to use the information we have learned to make something cool.

Let's make a very simple projerctile arrow using two objects.
I am going to use a triangle shape for the arrow head and a rectangle shape for a shaft.
- I will go ahead and create the first object by clicking on the 'Object' control bar button.
	- I now have a new object placed on the timeline. I will drag the timeline scrubber to overlap with the object so I can see what it looks like in the preview. I want to edit this object, so I will select it by clicking on it on the timeline, which brings up the Object Properties panel.
	- In that panel I will set its name to 'Arrow Head', which will help me identify what this object is in the future.
	- I am leaving the object type set to "Hit", so that it hits the player.
	- I should also make the object last longer, let's say 10 seconds. I will do that by setting the End Time value to 10. Notice that the object now appears longer on the timeline.
	- I want this object to be a triangle so I will change its shape by selecting the triangle category and then picking the triangle shape. You can see that change reflected on the preview.
	- At the moment the shape is very difficult to see due to its small size. Let's change that! To do so I must select the initial scale keyframe by clicking on it. It is marked as a small white diamond at the start of the scale keyframe timeline. Now that I have it selected, I will move over to the Scale Keyframe Editor above and set the X an Y values to be 5 units. Now the shape appears bigger in the preview. Don't worry much about keyframes yet, we will learn more about them in a later video.
	- Now, the triangle is pointing up, but I was imagining the arrow pointing left. I will rotate the triangle. For that I must select the initial rotation keyframe by clicking on it and then setting the rotation value to be -90 degrees.
- I think I'm done editing the 'Arrow Head' object, so I will create the next on—click on the 'Object' control bar button.
	- To edit the newly created object I select it by clicking on it.
	- In the Object Properties panel I will change this object's name to 'Arrow Shaft', leave the object type set to 'Hit', and change the End Time value to be 10 seconds.
	- I will change this shape's size by selecting the initial scale keyframe, and changing its values to be X 15 Y 2 units. As you can see in the preview the shape appears wide.
	- Currently the rectangle is on top of the triangle and they do not look like an arrow. I will align the rectangle by selecting the initial move keyframe, and changing its X in the positive direction, until it's aligned with the triangle in such a way that they form an arrow.
	- For convenience I will move this object down to the next line on the timeline by holding shift and clicking and dragging it down one line. Now objects don't appear to overlap one another on the timeline.
	I want both of the objects to appear and disappear at the same time. I can do that by clicking and dragging an object until their start is aligned.
		- If I wanted to do this more precisely, I could also select one of the objects, copy its Start Time property value, select the other object, and paste the value into its Start Time property.
	- Now if I drag the timeline scrubber back before the objects, and start playing the lever, you can see both of them appear and disappear at the same time.
Here it is! We made a simple arrow with two shapes!
Unfortunately, the arrow will remain static for now, but don't worry, we will definitely learn how to make it move in a future lesson.

## §5 🏃 Animation
Animation in Project Arrhythmia is what makes certain properties change over time. This is done using snippets of data called **keyframes**.

In Project Arrhythmia it is only possible to animate:
* Position, scale, rotation, and colour of objects,
* and Effects in the Effects & Checkpoints tab, which will be discussed in a future lesson.

I will create a new object to demonstrate how animation works. At the bottom of this object's properties panel you can see four coloured tracks labelled "Move", "Scale", "Rotation", and "Colour"—this is where I can animate this object. You can see that at the beginning of every track there is a little diamond shape—this is a **keyframe**.

Each keyframe holds a value. I can select the keyframe on the track labelle 'Rotate' and the editor will show me what value it holds in the keyframe editor at the top right. I can change that value to 20, and you can see this change beig reflected on the preview—the object is now rotated 20° counter-clockwise. I can select the keyframe on the track labelled 'Move', and I'll be presented with X and Y values for this keyframe. I can edit the value X to be 10 and you will see object's position is now 10 editor units to the right of where it was before.
Note that in Project Arrhythmia positX is right, and positive Y is up.

So, I changed the rotation and position of the object, but it is still not animated. That is because I only have one keyframe at the start of the tracks, and there is nothing to transition between.

Let's say I wanted my object to transition from right to left on the screen. I already have the first keyframe represent the position on the right, so I will create a new keyframe after the first one that will represent the position on the left. I do that by clicking with the right mouse button on the empty space of the 'Move' track, which makes a new keyframe appear behind the mouse pointer. I can click on it to select it and you will see the values it holds are the same as the first keyframe. To make it represent a position on the left I will change the X value to be -10. Now I have two keyframes for two positions on the screen—first right and then left.
If I play the level you can see the object move from right to left. How quickly the object transitions depends on the time between keyframes. I can change the second keyframe's position in time by either holding and dragging it on the track, or by selecting it and changing its Time to be later. As you can see the Time value for keyframes is represented by keyframe ticks, where 60 ticks is one second. You can see a little hint above the text field that shows how long the provided time is in seconds.
If I position the second keyframe to be at 90 ticks, which is a second and a half, after the first one, the transition between those keyframes will take a second and a half.

I can also change how the transition to a keyframe is animated with the Ease Type dropdown. Linear ease means the object will moveat a constant speed the entire transition, while Insteant easemakes the object immediately switch to the new values. There are many more available and you are free to explore how those ease types look.

Remember that every object has a keyframe at the beginning of every animation track? Those are **Initial Keyframes** and you cannot delete them or change their time.

Exclusively to position, scale, and rotation keyframes, you will see an additional property for each keyframe, which is **randomisation type**. This will be discussed very shortly.

Lastly, colour keyframes are a bit different from position, scale, and rotation keyframes. They do not allow for randomisation and have these values:
* **Colour** from the 'Objects' palette of the current theme. Themes will be discussed in a later lesson.
* **Gradient colour**, only if the object has a gradient enabled. If the colour of the gradient set to be the same as the first colour, then the gradient colour becaomes transparent.
* And **opacity**. Objects that aren't fully opaque will never hit players.

Keyframes have these properties that you can edit:
* Time — time of the keyframe, in ticks, where 60 ticks is one second
* Ease type — determines what easing method to use to interpolate between two keyframes
Transformation keyframes include these properties:
* Randomisation type — determines what type of randomisation to use, or none. Those will be explained in a moment.
* X and Y components — determines the position, scale, or rotation components to interpolate into. Position and scale are measured in units, while rotation is measured in degrees
Colour keyframes include these properties:
* Colour — which colour from 'Objects' palette in the current theme to use. Themes will be discussed in a later video in this series.
* Gradient colour — similar to the first colour. Only available for objects that have gradients enabled. If the selected gradient colour matches first colour, then the gradient colour becomes transparent.
* Opacity — controls opacity of the object, where 100 is fully opaque and 0 is fully transparent. Objects that aren't fully opaque will never hit players

### Randomisation
Randomisation makes the keyframes take random values every time the level is played.
There are 4 randomisation options:
* None — X and Y components act as normal
* Linear — uniform distribution. The game picks a random value between the "Min" and "Max" fields
* Toggle — "this-or-that", so to speak. The game picks either a "Min" or a "Max" field value
* Relative — or how I would call it "Multiplier" random. The game picks a random value between the "Min" and "Max" fields and multiplies both X and Y components by that number
Linear and Relative randomisation options have an additional Randmoise Interval field. If that field isn't zero, the random values are rounded to the nearest multiple of that interval value.
In the editor, you can re-roll the randomisation values by reloading the object using the Ctrl + R shortcut.

### Practice example
- Let's make our triangle appear by expanding out of nowhere. For that I'll create a new Scale keyframe here, by right clicking.
- I'll make the scale of the first keyframe (0, 0), and the scale of the second one (15, 15).
- Don't forget that you can move the scrubber within the animation timeline to change your current preview time.
- Now we have an animation like this.
- Let's change the ease type to use OutElastic. Now it's animated like this.
- Let's add a rotation keyframe, and make it rotate 360° with OutSine ease type.
- I will set this rotation keyframe's time to be the same as the last Scale keyframe so that the animation is synchronised.
- Now, let's give it a random position on the screen.
- I do that by selecting the first Position keyframe, and turning on Linear randomisation type.
- Let's say I want it to take a random position within the range of (-50, 50) for X and (0, 30) for Y.
  [[Demonstrate on video while narrating]]
- Now the triangle should only appear on the top half of the screen! You can preview different random positions by doing the Ctrl + R shortcut. [[Use it multiple times on video]]
- Now we can make it fade out after a few seconds by creating a colour keyframe here without changing any properties, so that the object stays the same colour through the first sequence.
- And another keyframe here, and setting its opacity to 0.
- And now we have an animation like this.
- Let's tell the game that we do not need this object anymore after the last keyframe by setting the End Time to be LastKF. While it didn't change anything visually, the game now knows when to offload the object for better performance in the level.
And now we have a very simple attack with a triangle that appears at a random location on the top half of the screen with a nice animation and fades out.

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

Parallax objects have some Events associated with them thta will be covered in a separate video in the series.

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