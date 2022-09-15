# AutoRotationBugiOS16
AutoRotation issue in iOS 16

This code demonstrates basic issue with iOS 16 Autorotation behavior(when not connected to debugger). It disables autorotation on startup and then after 0.2 seconds fires a notification to autorotate (in viewDidLoad method). In portrait mode, background color of view is set to orange. In landscape, it is set to green.

Below are the steps to run this app:

1. Hold an iOS device running iOS 16.0 in Portrait mode and connect to XCode debugger,
2. The app runs perfectly without any issues. The iPhone autorotates to portrait mode and background color of view changes to orange (as defined in code),
3. Next disconnect the app from debugger, kill and reopen the app by touching the app icon. Make sure iPhone is held in portrait mode in this step,
4. Autorotation fails, the background color of view remains green as function viewWillTransition(to size:, with coordinator:) is not called that does all orientation specific configuration for the view.

