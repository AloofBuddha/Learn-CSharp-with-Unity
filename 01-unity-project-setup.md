# 1. Unity - Environment Setup and New Project

I think we will have the best learning experience if we set up our Unity environment as our main testing environment for learning C#. We may rely on the console mostly at first, but it will be good to get comfortable in this environment if that is the main place we expect to be working ultimately. 

## Environment

* Download [Unity Personal Edition](https://store.unity.com/download?ref=personal) if you haven't already.

* We will use be using everything that comes standard with Unity for development, so that means our code editor will be MonoDevelop by default.

* It may be that certain additional things need to be downloaded (like .NET or xCode) so we will handle those too.

* Unity itself should warn us about any potential environment issues, but we'll do this together in person.

## Create a New Unity Project

> Unless otherwise stated, leave any defaults as they are!

* Open Unity

* Projects -> New

  - Project Name: `My First Project`

  - Location: `/Users/benjamincohen/Programming/Unity Projects`

  - Create Project
 
This creates the file structure Unity will use to create and maintain your project.

## Create/Save a Scene

 By default, there should be a new scene created, but unsaved. However, if no scene already exists, we can create one. 
 
* create a Scene if one doesn't exist already
  - File -> New Scene

* in the Hierarchy pane we should see a scene named 'Untitled' containing two pre-populated Game Objects: a directional light and a camera

* File -> Save Scene (or Cmd-S)

 - Save as "My First Scene" within the Assets folder (this is the default location)
 
Once this is done you should see the 'My First Scene' Scene populate in 'Project Pane' on the bottom.
 
### Overview

We should now have a basic Unity Project with a single scene, that contains a camera and a directional light, and nothing else. We can navigate to this project folder within Mac's Finder, to see that it really is just a folder, with some files we created and others created automatically by Unity. In general, we should only make changes to our Project within the Unity GUI, as making changes to the folder directly can often cause hard-to-catch bugs.

## The Unity GUI

Unity is a large application meant to do all types of 3D interactive work, and as such it can be a handful to learn at first, similar to an application like Photoshop. Before we get into coding, we want to familiarize ourselves with some aspects of the GUI.

### Layout

* Window -> Layout -> Default

This will setup the standard layout for Unity projects, which puts useful panes on our dashboard in a convenient layout. There are more panes then this and one's layout can be customized by dragging and dropping, but for now let's stick to the default.

#### Top Row

* To the left we have a number of different 'cursors' that allow us to manipulate the scene, such as grab, directional movement and rotate. 

* In the middle we have the play/pause buttons. This is how we will test our project by 'playing' it each time.

* To the right we have some features like collaboration and layers. These are relatively advanced features we can ignore for now.

#### Left Pane 

* to the left we have the Hierarchy Pane. This displays all the objects in the currently open scene. Everything in the Hierarchy Pane is a Unity 'Game Object'. It is called the Hierarchy Pane because we can nest Game Objects within each other for organization and other purposes. For now, we will not be nesting any Game Objects.

#### Middle Pane

* This is the 'main display'. It has two sub-panes: 'scene' and 'game'.

* The scene pane is where we can zoom in and out and rotate our view as a developer to manipulate the game world. Note that this is for the developer's convenience, but is unrelated to the 'Main Camera' Game Object that Unity will use in Play mode.

* By Pressing the 'Play' button we automatically switch to the game pane, which shows us what it would be like when our project is actually run. We can try it now, which should show us the persepctive of the Main Camera, however there isn't much going on in our scene now. Press 'Play' again when done to return to editing mode.

#### Right Pane

* This is the Game Object Inspector. Click one of the Game Objects currently in the Hierarchy Pane and you will see it populate with information unique to that Object. 

* Notice that both our Main Camera and Directional Light, despite serving very different purposes, have some attributes in common, such as a Name (a unique identifier for the object) and a Transform (the spatial information defining the Object). All Unity Game Objects have these attributes by default!

* We can manipulate these values directly to move/rotate our objects, or we can use the cursors in the top pane and manipulate the objects directly within the Scene view. 

> Note that some Transform attributes, like 'scale' don't seem to have any effect on our Main Camera or Directional Light. This is because neither of these Game Objects has any real dimension, only position and rotation. As stated above, Scale exists simply because all Game Objects have a complete Transform attribute, so when we create things like Spheres, this field will have an effect.

#### Bottom Pane

* The bottom pane is split into Project and Console.

* Project is where we can look through our directory structure for various assets we want to store. Unlike the Hierarchy Pane the Project View shows *all* assets, not just the GameObjects in a scene.

* The Console is likely where we will be doing a lot of our testing initially. It is simply a developer console for printing values. When the game is completed this will not be accessible by the end user, but it's useful for testing!

### Creating New Game Objects

Let's populate our Scene with two more Game Objects - a ground and a player.

 - Hierarchy -> Create -> 3D Object -> Plane

This will create a Plane object we should see in our Hierarchy view. When we select it, it's details should show up in inspector. To 'reset' the position of the plane to origin ({ x: 0, y: 0, z: 0 }) we can hit the 'gear' icon to the right of the Transform attribute and click 'reset'.

> In the hierarchy or inspector view we can rename our Plane to something more descriptive like 'ground'

 - Hierarchy -> Create -> 3D Object -> Sphere

Same as above, however note that the sphere is halfway between the plane! By default, this is fine in Unity as there is no 'collision' set (nor is there gravity, yet). 

To Do:

- Create a plane and name is ground
- create a sphere and name it player
- use the Transform attribute or the cursors to 
  - center the camera so we can see the full ground
  - raise the ball up so it's above the ground

### Creating a Material

You may have noticed that the 'player' sphere is difficult to see on the identically colored 'ground' object. Let's fix this by creating a new 'material' for the ground.

- In the Project pane select Create -> Material

- This should create a new Material in the Assets folder. I named mine Ground Blue and set the 'Albedo' attribute to a shade of dark blue.

- Drag the material from the Asset folder directly onto the Ground within the Scene View.

To Do:

 - adjust the directional light to see how it effects shading
 
 - play the project to see what the camera sees


## Conclusion

We are done with our basic environment! That was definitely a lot of information, but from this point on, we should be able to use these simple bits to learn C#!

## Next Time

* Unity Scripting
  - Adding scripts to game objects
  - the Start and Update 'hooks'
  - the 'print' method
  
* C#
  - review of essential syntax
  - variables, primitive types, public/private modifier
