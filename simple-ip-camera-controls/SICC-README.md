# Simple IP Camera Controls

This is a simple web app that allows you to control IP cameras.

## Features

- Add/Remove cameras
- Import/Export cameras
- Basic PTZ Camera Controls (Tilt, pan, zoom)

## Installation

1. Either clone the entire repo or download the `simple-ip-camera-controls` folder.
2. Open the `simple-ip-camera-controls.html` file in your browser OR create a custom dock in OBS and point the URL to the `simple-ip-camera-controls.html` file (example: file:///Users/username/downloads/simple-ip-camera-controls/simple-ip-camera-controls.html on Mac or C:\Users\username\Downloads\simple-ip-camera-controls\simple-ip-camera-controls.html on Windows).
3. That's it! 

## Usage

1. Add a camera by entering a friendly name for the camera (this can be anything you want), the IP address of the camera, the username, and the password.
2. Decide if you want/need pan/tilt/zoom controls.
3. Add any preset positions you want to use.  The ID must exactly match the preset name on the camera.  So if the preset is "track-1" on the camera it **must** match exactly (this is case sensitive).  The name can be anything you want.  The color is optional (defaults to gray) but you can add friendly color names (like "red", "blue", "green", etc.) or color codes (like "#FF0000" for red, you must include the #).
4. Click the "Add Camera" button.
5. You should now see the camera added to the list.
6. Use the controls to control the camera.

## Notes

- The username and password must have permission to control the camera.
- The preset positions are only available if the camera supports them.  Not all cameras do.
- The pan/tilt/zoom controls are basic and may not work with all cameras.
- Currently only AXIS VAPIX cameras are supported.