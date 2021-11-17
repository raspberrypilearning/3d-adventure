## Build and test

Now it's time to make your project. Start small, and add more to your project if you have time.

Image, gif or video showing what they will achieve by the end of the step. ![](images/image.png)


--- task ---

You have built up some really useful skills. Here is a reminder to help you make your project : 

### Unity reference

[[[unity-editor]]]

[[[unity-projects-scenes]]]

[[[unity-scene-navigation]]]

[[[unity-scene-top-down]]]

### Creating a 3D world

[[[unity-3D-coordinates]]]

[[[unity-plane]]]

[[[unity-3d-objects]]]


--- collapse ---

---
title: Create an object from a model
---

E.g. Tree

--- /collapse ---

[[[unity-transform-tools]]]

[[[unity-material-with-texture]]]


--- collapse ---

---
title: Child game objects
---



--- /collapse ---


### Add a player character

[[[unity-player-character-controller]]]

[[[unity-camera-follow-player]]]

### Add NPCs and other game objects

--- collapse ---

---
title: Create a game object that spins
---



--- /collapse ---

--- collapse ---

---
title: Create a game object that patrols
---



--- /collapse ---

--- collapse ---

---
title: Create a game object that follows a player
---



--- /collapse ---

--- collapse ---

---
title: Adding tags to game objects
---



--- /collapse ---


### Collisions and triggers

--- collapse ---

---
title: Use colliders to stop game objects occupying the same space
---



--- /collapse ---

### Variables and game states

--- collapse ---

---
title: Adding a public variable and changing it in the Inspector
---



--- /collapse ---

--- collapse ---

---
title: Updating a variable in a script
---



--- /collapse ---

--- collapse ---

---
title: Accessing another game object through a variable
---



--- /collapse ---

--- collapse ---

---
title: Keeping track of game state with variables
---



--- /collapse ---

### Scripting game objects

--- collapse ---

---
title: Print to the console
---

Debug.Log()

--- /collapse ---

--- collapse ---

---
title: Use colliders with triggers to detect when a game object collides with another game object
---



--- /collapse ---


--- collapse ---

---
title: Make a GameObject appear or disappear
---



--- /collapse ---

--- collapse ---

---
title: Checking conditions
---



--- /collapse ---

--- collapse ---

---
title: Organising scripts with methods (functions)
---


--- /collapse ---

### Sound and effects

[[[unity-play-sound]]]

[[[unity-add-soundtrack]]]

[[[unity-particle-system]]]

### Text and UI

--- collapse ---

---
title: Adding a name label to a game object
---



--- /collapse ---

--- collapse ---

---
title: Showing text in a 2D overlay
---

--- /collapse ---

--- collapse ---

---
title: Updating UI text in a script
---



--- /collapse ---

--- collapse ---

---
title: Enable and disable a canvas
---



--- /collapse ---

--- /task ---

--- task ---

**Test:** Show someone else your project and get their feedback. Do you want make any changes to your book? 

--- /task ---

--- task ---

**Debug:** You might find some bugs in your project that you need to fix. 

Useful debug tips:
- Turn on the Playmode tint so that you can tell when you are in game mode.
- Click on 'Gizmos' in Playmode and then click on a game object in the inspector to view its colliders.
- Look at the values of public variables in the Inspector in Playmode to see how they are changing. 
- Use `Debug.Log()` to print messages to the console to understand what's happening. 

Here are some common bugs.

--- collapse ---

---
title: I have a compiler error
---

Missing semi colon

Mismatched brackets

Can't find gameobject


--- /collapse ---

--- collapse ---

---
title: I made some changes but they have gone
---

Changes that you make in Playmode disappear when you exit Playmode. This is really useful when you just want to try something out. But, it's easy to accidentally make changes in Playmode - make sure you exit Playmode before making changes that you want to keep.

--- /collapse ---

--- collapse ---

---
title: My game objects are not positioned correctly 
---

Use the Transform tools to move around the scene and check your game objects from other angles. To change the position, use the **Move** tool or amend the `x`, `y`, or `z` position values in the Inspector **Transform** component.

--- /collapse ---

--- collapse ---

---
title: My game object does not show my new material
---

Look at your game object in the Inspector. Is your new material added as a component? If not drag it across from the Project window. 

--- /collapse ---

--- collapse ---

---
title: My game objects fall through the world when I run my scene
---



--- /collapse ---

--- collapse ---

---
title: My Main Camera doesn't follow my player correctly
---

Go to the **Hierarchy** window and make sure your Main Camera is positioned as a child of your player.

If your camera is following your player but not at the angle you want then you can look at the **Transform** component in the Main Camera's Inspection and update the `x`, `y`, or `z` position until you find an angle you are happy with. 

--- /collapse ---

--- collapse ---

---
title: My script has no errors but my game objects don't move
---

Look at the game object in the Inspector. Have you attached the Script as a component?


--- /collapse ---

--- collapse ---

---
title: My game objects pass through each other 
---

Unity uses colliders to provide physics for your game objects. Make sure you have added a **Character Controller** or a **Collider** component to your game objects.

--- /collapse ---

--- collapse ---

---
title: My script doesn't trigger when I collide with another game object
---

Make sure any characters/objects that you want to collide with have a **Box Collider** with `Is Trigger` selected.

If your characters/objects also have a **Character Controller** for collision detection you need to make sure that the **Box Collider** that triggers your script is of bigger scale so that you can get close enough to trigger it.  

--- /collapse ---

--- collapse ---

---
title: My patrolling characters do not move/face the right way
---

Think about the coordinates in your script: 
+ Are you moving along the correct `x`, `y`, `z` axis? 
+ Are you using the positive and negative values you need for your movement range.

Look at the character in the Inspector. Is your character rotated to face in the direction you wish to move?  

--- /collapse ---

--- collapse ---

---
title: My variables do not appear in the Inspector
---

Check that your variables are set up as **public** variables so that you can view them and edit their values in the Inspector. 

--- /collapse ---

You might find a bug not listed here. Can you figure out how to fix it?

We love hearing about your bugs and how you fixed them. Use the feedback button at the bottom of this page if you found a different bug in your project.

--- /task ---


--- save ---
