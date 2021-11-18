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

[[[unity-model-gameobject]]]

[[[unity-transform-tools]]]

[[[unity-material-with-texture]]]

[[[unity-child-gameobjects]]]


### Add a player character

[[[unity-player-character-controller]]]

[[[unity-camera-follow-player]]]


### Add NPCs and other game objects

[[[unity-gameobject-spin]]]

[[[unity-patrolling-gameobject]]]

[[[unity-follower-gameobject]]]

[[[unity-adding-tags]]]


### Collisions and triggers

--- collapse ---

---
title: Use Box Colliders to stop GameObjects occupying the same space
---

A 'Box Collider' has a simple cube shape that can be sized and positioned to stop GameObjects occupying the same space. 

To add a Box Collider, go to 'Add Component' in the Inspector window for your GameObject and select 'Box Collider'. 

Change the values in the 'Center' and 'Size' properties until you are happy that they are above the ground and cover the whole of your GameObject. 

Box Colliders will need to be added to all GameObjects that you want to avoid occupying the same space.

--- /collapse ---

### Variables and game states

--- collapse ---

---
title: Adding a public variable and setting it in the Inspector
---

When creating a variable in a script, you can declare it to be `public`. 

```
public float patrolSpeed = 0.0F;
```

This means that the variable will appear in the script component in the Inspector window. 

You can use the public variable during playmode to experiement with settings such as move and spin speed. Remember any changes you make in playmode will be lost when you exit playmode so take a note of your favourite values. 

**Tip:** Be careful when setting public variables in the Inspector window as this will override values set in your script. 

You can create many types of public variable such as `GameObject` variables so that you can access GameObjects from the scene:

```
public GameObject Player;
```

--- /collapse ---

--- collapse ---

---
title: Updating a variable in a script
---



--- /collapse ---

--- collapse ---

---
title: Accessing another GameObject through a variable
---



--- /collapse ---


### Scripting game objects

[[[unity-print-console-debug]]]

[[[unity-collider-trigger]]]


--- collapse ---

---
title: Make GameObjects appear or disappear using SetActive
---

You can use `SetActive(true)` to activate a GameObject and `SetActive(false)` to deactive a GameObject so that it doesn't appear. 


You can use `SetActive` on a public variable and drag a GameObject in the Inspector:

```
public GameObject heart;

void Start()
{
    heart.setActive(false)
}

public void PlayerReady()
{
    heart.SetActive(true);
}

```

You can also use `SetActive` on all GameObjects with the same tag:

```
public GameObject stars;

void Start()
{
    stars = GameObject.FindGameObjectsWithTag("Star");
    foreach (var star in stars)
    {
        star.SetActive(false);
    }
}

public void PlayerReady()
{
   IsReady = true;
    ButtonTime = Time.time;
    canvas.enabled = false;
    foreach (var star in stars)
    {
        star.SetActive(true);
    }
}

```

--- /collapse ---

--- collapse ---

---
title: Conditional behaviour with if/else
---

In C# you can use if/else statements to check conditions:

```
if (condition1)
{
  // code to run if condition1 is True
} 
else if (condition2) 
{
  // code to run if condition1 is false and condition2 is True
} 
else
{
  // code to run if condition1 and condition2 are False
}
```

You can use comparison operators to compare variables, numbers and strings: `<` `>` `==`.

You can join conditions together using Boolean and `&&` and Boolen or `||`.

Example:

if(transform.position.x < minPosition || transform.position.x > maxPosition)
{
    transform.Rotate(0, 180, 0); //turn around
}

--- /collapse ---



### Sound and effects

co

[[[unity-add-soundtrack]]]

[[[unity-particle-system]]]

### Text and UI

[[[unity-text-meshpro]]]

[[[unity-add-position-text]]]

[[[unity-npc-text]]]

[[[unity-button-with-onclick]]]

[[[unity-textmeshpro-variable]]]

[[[unity-update-textmeshpro]]]

--- /task ---

--- task ---

**Test:** Show someone else your project and get their feedback. Do you want make any changes to your book? 

--- /task ---

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">"Play your game while you’re writing it. Play it a lot. Play it over and over. Every time you start work on your game again, begin your work session by replaying." - Emily Short, Game Narrative Designer</p>

--- task ---

**Debug:** You might find some bugs in your project that you need to fix. 

Useful debug tips:
- Turn on the Playmode tint so that you can tell when you are in game mode.
- Click on 'Gizmos' in Playmode and then click on a game object in the Inspector to view its colliders.
- Look at the values of public variables in the Inspector in Playmode to see how they are changing. 
- Use `Debug.Log()` to print messages to the Console to understand what's happening. 
- Check the Console for errors. Script errors also appear in the bar at the bottom of the editor. 

--- collapse ---

---
title: I have an error in the Console
---

Check 

+ '; expected' - check for a semicolon `;` at the end of each line of code. 
+ 'Newline in constant' - you missed a quote `"` from the end of a text string.
+ '} expected' - you should have a pair of open and close curly brackets `{}` around each method and around the class. Check that your curly brackets match.
+ ') expected' - make sure there's a closing `)` at the end of each Method call, before the semicolon.
+ 'Debug' does not contain a definition for 'log'' - C# is case sensitive, it needs to be `Log` with a capital `L`.

**Tip:** Double-click on a code error in the Console to go straight to the line of code that is causing the problem.

--- /collapse ---

--- collapse ---

---
title: I made some changes but they have gone
---

Changes that you make in Playmode disappear when you exit Playmode. This is really useful when you just want to try something out. But, it's easy to accidentally make changes in Playmode - make sure you exit Playmode before making changes that you want to keep.

--- /collapse ---

--- collapse ---

---
title: My GameObjects are not positioned correctly 
---

Use the Transform tools to move around the scene and check your game objects from other angles. To change the position, use the **Move** tool or amend the `x`, `y`, or `z` position values in the Inspector **Transform** component.

--- /collapse ---

--- collapse ---

---
title: My GameObject does not show my new material
---

Look at your game object in the Inspector. Is your new material added as a component? If not drag it across from the Project window. 

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
title: My script has no errors but its methods are not running
---

Make sure the script is attached to a GameObject. Have you attached the Script as a component?

If the script uses `OnTriggerEnter` or `OnTriggerExit`, make sure the GameObject has a collider with 'Is Trigger' selected. 

--- /collapse ---

--- collapse ---

---
title: My GameObjects pass through each other 
---

Unity uses colliders to provide physics for your GameObjects. Make sure you have added a **Character Controller** or a **Collider** component to your GameObjects.

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
