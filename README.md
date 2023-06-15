# Gyro-Unity
An archive to document sources, references and examples of gyroscopic input into a Unity project.

## Build for Windows

First, upgrade to the Unity [Input System Package](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.6/manual/index.html). Use the Package Manager to update, and in Project Settings -> Player -> OS -> Other Settings -> Active Input Handling, change to the newer system. Check that Input Manager is disabled in the settings.

In Project Settings -> Input System Package, Create a new settings asset.

![Settings Asset](https://connect-prd-cdn.unity.com/20201207/learn/images/f40d3341-d1a4-49dc-ac68-20ca4a21dd74_tut1_12.png.1400x0x1.png)

Add Component "Player Input" to the player model.
In Player Input, Create Actions, and save the file with the assets.








## [Reference Video: Unity- how to make a player controller with gyroscope and accelerometer](https://youtu.be/jvwX5WthM2o)

**This project was meant for Android mobile.**

In Unity, File -> Build Settings

  Switch platform to Android. Download required Android module from Unity Hub, if necessary.
  
  ![Build Settings](Saved%20Pictures/buildSettings.png)
  
Project template should include a 3D Plane Object for the Ground and a Capsule 3D Cylinder for the player model.

  Add a Character Controller component on the player model.
  
  In the Assets/Scripts folder of the project, create a C# Script called *PlayerController.cs*, and add the script as a component to the player model.
  
  Drag the Character Controller component to the Controller menu in the Player Controller script component.
  
  In Unity, Edit -> Project Settings -> Adaptive Performance, check the necessary Android Providers.
  
  In Unity, Edit -> Project Settings > Player > Android (Tab) > Publishing Settings > Custom Gradle Properties Template
  
  Delete all files in: C:\Users\you\.gradle\caches
  
  In Unity, Edit -> Preferences -> External Tools
  
  Update in Window -> Package Manager
  
  Adjust Version number and Project Name at File -> Build Settings -> Player Settings -> (Bundle Version Code)
  
  Copy all folders and files inside Editor/Data/PlaybackEngines/AndroidPlayer/SDK/cmdline-tools, create a new folder called Tools inside AndroidPlayer folder and paste there.
  
  The problem is that the SDK folder needs to be readable on Windows explorer, and Windows always makes the folder read-only automatically. I used to be able to make the folders non-read-only which made my code compile, but now it is not letting me change the status of the SDK from read-only to readable. 
  
   Copy the SDK folder to documents, unitick the read only, and change SDK the folder on Unity preferences. Apparently there is a lock on the usual unity java SDK folder. 

### General Tips

To check controller input:

Window -> Analysis -> Input Debugger

[Gradle Build Failures](https://support.unity.com/hc/en-us/articles/4408584577044-Why-do-I-get-errors-when-using-a-Gradle-file-with-an-old-aaptOptions-noCompress-property-)
