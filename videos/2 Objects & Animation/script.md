## 📦 Gameplay Objects & Animation
Now that you know how to navigate around the editor, let's begin creating something more interesting. And to do that we will start with a gameplay object, because they're the most essential part of gameplay and decorations of any level.
Let's play the music from the beginning and think of what attack could go here...

> *Synth waaaa...wa, wa, waaa~ type sound*

Sounds like something spinning to me, and I think I can visualise a spinner attack that could go here. It looks like a quarter circle that is spinning and changing direction to the wawawa sound.
I'll create a new object by clicking on the "Object" button on the control bar. I could also create one with these presets in the little pop-up, but I never find myself actually using it.

Before doing anything else, let me make the shape larger by clicking on the first scale keyframe and changing its values to X 20 Y 20.

##### Properties rundown
Let's go through what all of these options mean over at the object properties panel, and change some of them.
* At the very top above the name we have 6 **colour coding** toggles. These change how objects are coloured on the timeline, purely for editing purposes. The toggles are additive, so if I have the Blue and Red ones on, the colour on the timeline changes to Purple.
* Next one is the **Name**, which also just changes the label of the object. I'll call it "Spinner circle attack" and you can see the label change to reflect that.
* The next property is **Type** of the object. That's what determines its function. There are three types to choose from:
	* Hit - The object will hit players on collision, if fully opaque. It is used for obstacles which is what I want, so I will leave it set to Hit.
	* No hit - The object will never hit players. It is used for decorations.
	* and Empty - the object will be invisible and won't hit players. It is used for parenting, which will be discussed in a later lesson.
* Next up we have **Start Time**, which is the same as dragging object's label left or right, but you work with precise time in seconds here. I will move the object start to where the wawawa sound starts first.
* Then comes **End Time**. This is what tells the game when the shape is no longer needed, making it disappear and helping reduce lag. I like changing this last so we will come back to that later.
* Next we have **Shape**, which presents you with 6 categories of shapes. I wanted to make my attack a quarter circle, so I'll click on a circle category, and choose a shape that looks like a quarter of a circle.
* Right below you get a choice of 5 **Gradient** types. I will select the radial one. A little drop-down will appear for adjusting the gradient, but I think it already looks good so I won't touch it.
* **Render Depth** controls whether the shape appears in front of or behind other shapes.
* **Parenting** lets this object inherit certain properties of another object. It's a very important and complex subject so it will have its own lesson in the series.
* Scrolling down we're presented with **Editor Layer** and **Editor Bin** properties. These are purely for editing convenience and won't be apparent in the level.
* Next is **Shape Origin** which controls the centre of the shape. It's useful for rotation and scaling around a certain point in the shape. I'll leave this as defaults.
* And lastly, **Keyframes Timeline** where you can animate position, scale, rotation, and colour properties of the shape. When you create a new object it has 1 initial keyframe for every line on the timeline, at the very beginning. You can't move or delete these initial keyframes.

##### Animation
I wanted my attack to spin. Let's add a **rotation** keyframe by clicking on empty space in the keyframe timeline with the right mouse button.

Do note that you can only create new keyframes below the dark area that you can see above the timeline. I don't know why that's the case, and it's silly, but it is what it is.

I will change its Rotation value to 360°.

If we play the level you can see the shape slowly rotates full circle at a constant rate. What if I wanted it to start fast and slow down to its new rotation? For that I will change the **Ease Type** of the keyframe. Expanding the drop-down presents us with many easing types to choose from, but I will go with OutSine, which matches my desired rotation rate. You can play around with these and see how they're different from one another.

I want my attack to change spinning direction to the music, so let's time this keyframe to the end of the first 'wa' sound. I will slow down level playback from the Control Bar to—let's say—0.5 speed, and play the level to see where I should put the keyframe.

Here! I'll drag the keyframe to this position.

I will create a new rotation keyframe and set it to spin in the opposite direction by setting it's value to -700°, and time it to the end of the next 'wa' sound. Then another one, spinning 800°, also timed, and the last one, set to -1000°.

Let's reset the speed to 1.0 and play the level from the beginning... Isn't this amazing?

I don't like how my attack just suddenly pops in, does it's thing, and suddenly disappears. Let's add a fade in and fade out for this attack.

Colour keyframes define main colour, gradient fade colour, and opacity of the shape. I will select the initial colour keyframe and change its opacity to 0%, then create a second colour keyframe with opacity set to 100%. This fade in also serves a second purpose, because the attack will only hit the player when the opacity is at 100%, so players have time to react to this attack.

To create a fade out I will create another keyframe where I want the fade out to begin, and leave opacity at 100%. Doing so give this object time to stay fully opaque between the keyframes. I will then create a keyframe where I want the fade out to finish, and set its opacity to 0%.

Now the attack looks like this. *(plays level)*

##### Randomisation
I will change its first position keyframe to appear somewhere else other than the middle-centre, but I will do something clever here and make the position random! For that I will select initial position keyframe and turn on **Linear** randomise type. Now instead of providing just the X and Y coordinates I can provide ranges.

I want the random range to include most of the screen. To quickly get needed coordinates I can toggle the **Grid** by navigating over to the Menu Bar, View, and choosing "Toggle Grid". As well as showing the grid lines, the editor now shows coordinates of the position my cursor is hovering over, in the top-right corner of the preview.

I'll hover over the bottom-left edge of the preview and put the coordinates as X and Y minimums of the keyframe. X-min -47 and Y-min -24. For X-max and Y-max I will put the coordinates of the top-right corner of the preview. X-max 47 and Y-max 24.

Every time a player starts my level this shape will appear at a different location on the screen. I can quickly preview a different randomisation possibility by having the object selected and performing Ctrl + R re-randomisation shortcut.

Before moving on I want to quickly explain other randomisation types.
* Linear type picks any position in the provided ranges and **Randomise Interval** will round the rolled value to the nearest provided multiple.
* Toggle type—"this-or-that" so to speak—will only pick between two positions provided.
* and Relative type will pick a number in the provided multiplier range, rounding it to the nearest multiple of **Randomise Interval** value, and multiplying both position X and Y with that value.

##### End Time
I think I am finished with this attack. Remember I mentioned End Time property earlier? This property helps the game know when to remove the shape to optimise the level.

It has 4 options:
* Last Keyframe will make the shape disappear immediately after its animation ends.
* Last Keyframe Offset is the same, but lets you specify a delay in seconds.
* Fixed Time will make the shape disappear the specified amount of seconds after its start,
* and Song Time will make it disappear when a specified amount of time into the song is reached. If the object starts after this time then the shape will never appear.

I don't need this object after its animation ends, so I will select Last Keyframe.

##### Multiple objects
Let's reuse this attack for the rest of the wawawa sounds in this section. I will duplicate this object by having it selected and using Ctrl + D duplication shortcut, and then dragging its label over to where the next set of wawawa sounds starts. Don't forget to check whether the attack is still synchronised with music by quickly playing the level.

I will duplicate this object again but keep its start position the same to make players dodge two attacks at once.

I will do the same for the next set of sounds with even more attacks appearing simultaneously, continuing this pattern to the end of this section.

Let's move back to the beginning play-test the level. For that I will hover over the **Play Testing** button at the end of the Control Bar and press "Normal". *(Plays the level)*

Splendid! I can leave play testing mode by hitting Escape and save my level.

##### Conclusion
This concludes this lesson on Gameplay Objects and Animation. We went over important topics like what gameplay objects are, their properties, animation keyframes, keyframe easings, and randomisation.

Don't forget that if you feel overwhelmed you're not alone. The learning curve for the editor looks like the icon for OutCirc easing, and you're slowly getting over the initial struggle. As always, feel free rewatch this video if you have any problems, don't forget to ask for help in the comments, Steam Discussion forums, or in the official Project Arrhythmia Discord server, people will gladly help you there.

Make it a great week by being kind to others. New high score, enter your name below.
