## 👋 Introduction
> *Montage of some cool Project Arrhythmia levels*

This is Project Arrhythmia. A fun rhythm bullet-hell game in which all things beautiful are deadly. The game has a broad library of thousands of challenging, beautiful, and creative levels made by members of its community.
> *The montage zooms out to show the levels are being previewed in the editor*

One of the appealing features of this game is its robust level editor used to create all these levels.

Whether you're a new or a returning creator and you want to learn how to make a Project Arrhythmia level like *this*, or *this*, or *this*, then you're in the right place.
> *Recording of a level that will be created and finished in the tutorial*

In this tutorial I will explain the basics, walk you through creating this simple level you see on the screen, and by the end you will have enough knowledge to start making and publishing your own creative levels.

You can find useful links and update notes in the description of every video, also every video has captions available.

Now, forget about N-Chan. Today *I* will be your guide to the Project Arrhythmia editor...

## 🚧 Making a New Project
![(Level creation screen screenshot)](assets/welcome-create-level.png)<br>
##### Song
First things first, we need to choose what song to use for our level. For new creators I recommend going with something fairly short and simple at first.

One important thing to note is that if you're planning to publish your level, make sure the song you're going to use is verified for use in Project Arrhythmia, otherwise it will be removed by moderators after being published. I will link information about that in the description.

In this tutorial I will be using [‘Sphero’ by Xtrullor](https://www.newgrounds.com/audio/listen/612751) which is both verified and free to download. I'll link the download page in the description as well.

##### Create
To start creating we will need to make a new project. Open up the editor by selecting ‘Creation engine’ in the main menu, then switch to the ‘Create level’ tab on the sidebar.

You will be asked to fill in a few fields with information about the song and your level. Make sure to get them right, otherwise the song artist will be sad, and we don't make artists sad in Project Arrhythmia.
* I will give this level a title, which will be ‘My first level’. This can be anything you like.
* For **‘Song Title’**—since I'm using Sphero made by Xtrullor—I'll put ‘Sphero’, because that is the title of the song, obviously.
* And the **‘Song Artist’** will be ‘Xtrullor’.
* ‘Audio file location’ — here you click ‘Browse’ and choose the song file. ‘Sphero.mp3’. Do note that the editor is a bit quirky with some ‘mp3’ files and might not create the project properly, in which case you'll have to use a different file format.
* ‘Level artwork’ — this is where you select a level icon. The icon should be a ‘.jpg’ image no bigger than 512 pixels squared. I will leave it blank for now, I can always set it later.
* ‘Level background setup’ lets you create a level with a background preset. I will select ‘City’ because I think it's pretty.

Click the ‘Create new level’ button. And a new empty project is created. Let's pause the playback, and welcome to the editor!

## 🖼 Overview
![(Editor interface overview)](assets/overview.png)<br>
##### Editor Interface
Now that we have a project loaded, let's take a look at the main interface of the editor. It is divided into multiple distinct windows.

##### Level Preview
So, this big view on the top-left is the **‘Level Preview’**. This is where you can see how your level looks at any given time and this is what the players will see when playing your level. You can control the current time of the preview by dragging around the blue handle at the bottom like this.

I'll drag it all the way to the very beginning and you can see there is a square shape moving around on the preview as I'm doing that. This is a ‘gameplay object’. I can click on its shape to select it.

##### Property Editor
Now, what if I wanted this shape to be a circle? I can do that by using the **‘Property Editor’** window to the right of our Level Preview. This window is different depending on what you have currently selected. If I select any of the dark squares—which are background or ‘parallax’ objects, by the way—the property window will show properties specifically for parallax objects.

So if I want to change the shape of the gameplay object I will select it by clicking on it, go over to the ‘Shape / Gradient’ section, click on one of the 6 shape categories, for example, a circle, and choose a simple circle from the pop-out.

Some properties like position, scale, rotation, and colour have their own animation timeline which is shown at the bottom of this window, which we will get back to in a minute.

By the way, don't worry about all the other properties yet. In this video I'm only going over the main interface of the editor.

##### Timeline
Next thing I'm gonna show you is the **‘Timeline’** that spans the entire bottom half of the editor. The timeline is where we can see a representation of all of the gameplay objects in the level placed at specific points in time, shown as **‘Object Labels’**, which we only have two of right now. I can click on a label in this window and that will select the object just like clicking on its shape in the Level Preview did.

If I press play you will see the blue handle starts moving to the right, indicating that the time is advancing. We call this blue handle a ‘Scrubber’. By the way, the shortcut to play or pause the level is Spacebar.

The length of a label on the timeline represents how long the object appears on the screen for. If the scrubber is on top of a label, that means that object is visible at the current time. I can change when this object appears in the level by dragging its label around the timeline.
I can hold ‘shift’ while dragging to move the label up or down, but it won't change anything about the actual level, it just makes it easier to organise your objects.

##### Property Editor (Keyframes)
Now, let's come back to the four special properties of gameplay objects. Did you notice that our object has an animation where it slowly moves to the right and then back? So why is that? If I select the object and look at its animation timeline... ah! There we have a line labelled ‘Move’ with funny diamond shapes on it. These diamonds are what we call ‘Keyframes’ and they define specific values to transition between.

So, this object has three ‘move’ keyframes. I can click on one to start editing its values in the top-right portion of the window. The first keyframe defines position X 0 Y 0, which is the middle centre, the second keyframe defines position X 10 Y 0, which is just to the right of that, and the third keyframe defines position X 0 Y 0 again. Let's edit the position of the second one to be X 10 Y 10 and play the level. As you can see, the object is now moving diagonally from the centre and back.

I can change the timing of keyframes by selecting and dragging them left or right, or by modifying their ‘Time’ property.

I can create new keyframes by clicking with the right mouse button on an empty space, delete keyframes by having them selected and using the ‘Delete’ key, and zoom in and out both of the timelines by hovering over one and using the shortcuts ‘\[Ctrl\]+\[+\]’ and ‘\[Ctrl\]+\[-\]’.

Another fun way to create a new keyframe is by clicking and dragging the object around right in the level preview! That will immediately create a new keyframe at the position of the scrubber, or update it if there is one already.

There are 4 dragging modes that can be used with 4 keyboard keys: \[W\] for position mode, \[E\] for scale mode, \[R\] for rotation mode, and \[T\] for colour mode. Your current dragging mode is displayed at the top-right corner of the level preview.

##### Control Bar
So now you know how to work with one gameplay object, but there's only so much you can do with just that, so let's create another one. For that I will use the **‘Control Bar’** which is situated right below the Preview Window. The Control Bar lets you do things like control playback, change the timeline layer, and create new objects. So to create a new gameplay object I simply click on the button that says ‘Object’, and here it is, in the middle-centre of the preview. It's so small, let's make it bigger by changing the drag mode to ‘size’ with ‘E’, and dragging from it in the preview.

If I want to delete an object I would select it either by clicking on its label on the timeline or its shape in the preview, and using the ‘Delete’ key.

##### Menu Bar
Let's say I want to save my project. For that I would use the **‘Menu Bar’** at the very top of the interface. I click ‘File’ and then ‘Save Level’, or simply use the ‘\[Ctrl\]+\[S\]’ shortcut. You can see the list of other useful shortcuts under ‘Help’, ‘Key Shortcuts’.

It is important to remember to save your progress often, as Project Arrhythmia is still in Early Access and has some bugs that could cause crashes.
The game also saves a backup of your level periodically, and those will be discussed in a later lesson.

When it is time to come back to working on a level after a nice break, you can always open the level project from the welcome screen by finding it in ‘Recent Levels’ section in the ‘Home’ tab, or in the ‘Open level’ tab.

##### Getting Help
Lastly, I'd like to say that if you find any of this very difficult—don't worry. Level creation has a bit of a learning curve and you're right at the beginning of it, so if you keep going you will quickly get over the initial struggle. You can also ask for help in the YouTube comments, Steam Discussion forums, or in the official Project Arrhythmia Discord server, people will gladly help you there.

Thank you for watching! Make it a great week by being kind to others.