# Internet-of-Things-Department-Task-1
1st task of Internet of Things Department - Summer training program at Smart Methods


![image](https://github.com/H16Bw/Internet-of-Things-Department-Task-1/assets/139852537/6982b844-5557-4d8c-9a37-d75b06d16256)

The attached code is an Arduino program that controls a robot connected to a WiFi network. The robot receives commands from a server and executes them using Arduino to control its motors. To rewrite the code in the same way, we need to provide the required Arduino libraries and specify the WiFi network data (WiFi name and password) and the URL addresses for the robot's requests.

Before running this program, make sure to install the required Arduino libraries from the library manager in the Arduino IDE.
The code includes libraries like WiFi, HTTPClient, and Serial, which should be installed.

Replace "YOUR WiFi Name" with your WiFi network name and "WiFi Password" with your network's password. Additionally, modify the URL addresses for the GET requests based on your robot's needs.

The code repeatedly calls the server and executes commands with a specified time interval (5 seconds), and you can adjust this time interval if necessary.

One example of running this program is to place it in a robot control unit connected to the internet, where the server can be called from any internet-connected device to send commands to the robot to control its movements and make specific decisions.
