## Gamepad Printer Control
This Python script allows you to control your OctoPrint-enabled 3D printer using a joystick or gamepad. The script uses the **pygame** library to read input from the joystick and sends commands to the OctoPrint server using the **requests** library. Here is a link to a youtube [video](https://www.youtube.com/shorts/IK1qhjoYjms)

## Requirements
- Python 3
- requests library
- pygame library

You can install the required libraries using pip:

```bash
pip install requests pygame
```

## Configuration
Before running the script, you need to configure the following variables in the script:

- `octoprint_ip`: The IP address of your OctoPrint server.
- `octoprint_port`: The port number of your OctoPrint server.
- `api_key`: The API key of your OctoPrint server.

You can find these details in the settings of your OctoPrint server.

## Usage
To run the script, navigate to the directory containing the script in your terminal and run the following command:

```bash
python octocontroller.py
```

The script will start a loop that reads input from the joystick and sends commands to the OctoPrint server. The X and Y axes of the joystick are mapped to the X and Y axes of the printer, and the buttons are mapped to various commands.

## Button Mappings

It is currently set up for using the joysticks, triggers and face buttons of an Xbox controller.
- Left joystick Y-Z
- Right joystick X-E0 (Tool0)
- L/R Triggers E1 (Tool 1)
- A/B Open/Close Gripper

## Throttling
The script includes a delay of 0.2 seconds at the end of each loop iteration to throttle the input from the joystick. You can adjust this delay to suit your needs.
