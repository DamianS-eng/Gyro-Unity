# Gyro-Unity
An archive to document sources, references and examples of gyroscopic input into a Unity project.

## Build for Windows

First, start a 3D core template from the latest version of Unity. Import [this starter asset](https://assetstore.unity.com/packages/essentials/starter-assets-third-person-character-controller-urp-196526) from the Unity asset store. This asset will upgrade to the Unity [Input System Package](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.6/manual/index.html) and cinemachine camera. Use the Package Manager to update, and in Project Settings -> Player -> OS -> Other Settings -> Active Input Handling, change to the newer system. Check that Input Manager is disabled in the settings.

## If Imported Assets are purple:

You need to set up the project to use the Universal Render Pipeline asset from the Asset package.

To upgrade built-in Shaders:

Open your Project in Unity, and go to Edit > Render Pipeline > Universal Render Pipeline. 
According to your needs, select either Upgrade Project Materials to UniversalRP Materials or Upgrade Selected Materials to UniversalRP Materials.
Open your Project in Unity, and go to Project Settings > Graphics > URP Global Settings. If needed, select Fix.

## Initial Camera Setup from Cinemachine



### General Tips

#### To check controller input:

Window -> Analysis -> Input Debugger

[Gradle Build Failures](https://support.unity.com/hc/en-us/articles/4408584577044-Why-do-I-get-errors-when-using-a-Gradle-file-with-an-old-aaptOptions-noCompress-property-)
