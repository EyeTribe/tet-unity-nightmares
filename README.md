Nightmares Unity Sample for The Eye Tribe Tracker
====
<p>

Introduction
----

This is a modified version of the [Unity 4.6](http://unity3d.com/) sample project 'Nightmares'. This variant uses eye tracking input from The Eye Tribe Tracker to add unique features to the game.

![](http://theeyetribe.com/images/nightmares_1.png)

The gameplay of the sample has been altered to use gaze input. 

- Avatar is moved using *arrow keys* or *joystick*
- Firing is done using *ctrl* or *joystick Fire 1*
- Aiming is done using *eye coordinates* (instead of normal mouse position) 


**Improvements**<br>
In its current state, this sample does _not_ resolve all issues related to using eye input for game control.  Since eye gaze can jump from one corner of a screen to the opposite in a very short time, special input handling may be needed. The Eye Tribe encourages developers to improve the overall experience by introducing they own solutions to these issues.


Modifications
----

The following files from the original sample have been modified. Changes to the original script files are tagged with /* @TheEyeTribe */

- ./Assets/Scripts/Player/PlayerMovement.cs
- ./Assets/Scripts/Player/PlayerShooting.cs
<br/>

The following scripts were added to the sample:

- ./Assets/TheEyeTribe/EyeTribeUnityScript.cs
- ./Assets/TheEyeTribe/GazeDataValidator.cs
- ./Assets/TheEyeTribe/UnityGazeUtils.cs
- ./Assets/TheEyeTribe/CalibCamera.cs

The *EyeTribeUnityScript* was attached top the Main Camera of the game scene.

Minor change in *Build Settings* was required to use [EyeTribe C# SDK](https://github.com/EyeTribe/tet-csharp-client). *Player Settings -> Windows -> Other Setting -> Api Compatibility Level* must be set to .NET 2.0


Dependencies
----

This sample has been developed in Unity 4.6 and uses the [EyeTribe C# SDK](https://github.com/EyeTribe/tet-csharp-client). 


Build
----

To build, open project in [Unity](http://unity3d.com/) and build for Windows OS or Mac OSX.

Note that the EyeTribe Server currently supports Windows 7 and newer as well as Mac OSX 10.8 and never. Support for other platforms will be added in the future.


FAQ
----

Should question arise, do not hesitate to post them on [The Eye Tribe Forum](http://theeyetribe.com/forum/).


Changelog
----

0.9.49 (2014-12-12)
- Initial release
