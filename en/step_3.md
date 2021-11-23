## Build and test

Now it's time to make your 3D Adventure. Start small, and add more to your 3D adventure if you have time.

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

[[[unity-physics-colliders]]]


### Variables and game states

--- collapse ---

---
title: Adding a public variable and setting it in the Inspector
---

When creating a variable in a script, you can declare it to be `public`. 

```
public float patrolSpeed = 0.0f;
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
title: Accessing another GameObject through a variable
---

To access a variable from another GameObject, that variable must be public:

```
public class StarPlayer : MonoBehaviour
{
    public int stars = 0; 
}
```

You can then create a variable with the type of the script that has the variable and set it using the Inspector. You will then be able to access the variable to read the value or update it. 

```
    StarPlayer player;

    void AddStar()
    {
        player.stars += 1; // increase by 1
    }

```

--- /collapse ---


### Scripting game objects

[[[unity-print-console-debug]]]

[[[unity-collider-trigger]]]

[[[unity-setactive]]]

[[[unity-conditional-scripting]]]


### Sound and effects

[[[unity-play-sound]]]

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

[[[unity-console-error]]]

[[[unity-changes-gone]]]

[[[unity-assign-material]]]

[[[unity-camera-error]]]

[[[unity-method-absent]]]

[[[unity-collider-error]]]

[[[unity-trigger-error]]]

[[[unity-show-variables]]]

--- collapse ---

---
title: My patrolling characters do not move/face the right way
---

Think about the coordinates in your script: 
+ Are you moving along the correct `x`, `y`, `z` axis? 
+ Are you using the positive and negative values you need for your movement range.

Look at the character in the Inspector. Is your character rotated to face in the direction you wish to move?  

--- /collapse ---

You might find a bug not listed here. Can you figure out how to fix it?

We love hearing about your bugs and how you fixed them. Use the feedback button at the bottom of this page if you found a different bug in your project.

--- /task ---


--- save ---
