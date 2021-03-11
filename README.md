# viveproeye
VIVE Pro Eye Testing Practices

## 1. Setup Guide
First, set up your headset
Follow the VIVE Pro Eye Setup guide.
https://enterprise.vive.com/eu/setup/vive-pro/

## 2. Calibrate for your eyes
The VIVE Pro Eye Setup guide will automatically start the calibration at the end of the setup flow.
If you need to re-calibrate or if you switch users, you can always open the calibration tool from the SteamVR dashboard.

## 3. Download and Import the VIVE SRanipal SDK
Download the VIVE SRanipal SDK and import the .unitypackage into your Unity project.

https://developer.vive.com/resources/vive-sense/sdk/vive-eye-and-facial-tracking-sdk/

Make sure the VIVE Sranipal SDK works before going to the next step.
The tray icon eyes turn green when eye tracking is active, this should happen when your Unity application is running.

## 4. Import the Tobii XR SDK
Download the Tobii XR SDK for Unity and import it into your Unity project.

https://vr.tobii.com/sdk/downloads/

Remember to enable VR support in your Unity project. We support Unity 2018.2.5f1 or later.
If you have an older version of the Tobii XR SDK, remember to remove it before importing the new version to avoid conflicts.

## 5. Add the TobiiXR Initializer prefab to your scene
The prefab can be found in the Prefabs folder.
The TobiiXR_Initializer script attached to the prefab calls TobiiXR.Start() to initialize the the Tobii XR SDK.

## 6. Configure the Tobii XR SDK
To configure the Tobii XR SDK, edit the fields of the TobiiXR Initializer prefab in your scene.

1. Make sure the VIVE provider is at the top of the Eye Tracking Providers list.
2. Enable the Support VIVE Pro Eye option.

More information at https://vr.tobii.com/sdk/develop/unity/documentation/tobii-settings/

## 7. Create a cube and place it somewhere in the scene

## 8. Add the HighlightAtGaze script to the cube
The HighlightAtGaze component implements the IGazeFocusable interface, which will be called whenever the object receives or loses focus.

## 9. Run the scene
By pressing play, you can now highlight the cube by looking at it.

If you want, you can add more objects that react to gaze to the scene in order to test and play around.

