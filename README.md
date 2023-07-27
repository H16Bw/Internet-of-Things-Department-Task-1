# Internet-of-Things-Department-Task-1
1st task of Internet of Things Department - Summer training program at Smart Methods


![image](https://github.com/H16Bw/Internet-of-Things-Department-Task-1/assets/139852537/6982b844-5557-4d8c-9a37-d75b06d16256)

This code is an Arduino program to remotely control four LED lights using Wi-Fi connection. The program checks for Wi-Fi connection and then sends HTTP GET requests to four different URLs on the internet.

When the program starts, it attempts to connect to the specified Wi-Fi access point (the network name and password are set using wifiMulti.addAP()). After successfully establishing the connection, it sends HTTP GET requests to specific URLs.

The four URLs are:

https://s-m.com.sa/f.html: Represents the movement "forward."


https://s-m.com.sa/r.html: Represents the movement "right."


https://s-m.com.sa/l.html: Represents the movement "left."


https://s-m.com.sa/b.html: Represents the movement "backward."

When the device receives a response from the server at each URL, it reads the response (payload) and compares it with the keywords "forward," "right," "left," "backward," or "stop," depending on the used URL. 

When a match is found, the corresponding LEDs connected to pins 25, 26, 27, and 32 will be turned on, and the others will be turned off.

Example of operation:

If the response is "forward," the LED connected to pin 27 will be turned on, and the others will be turned off, indicating that the robot is moving forward.


If the response is "stop," all LEDs will be turned off, indicating that the robot has stopped moving.

# NOTE:

The attached code is an Arduino program that controls a robot connected to a WiFi network. The robot receives commands from a server and executes them using Arduino to control its motors. To rewrite the code in the same way, we need to provide the required Arduino libraries and specify the WiFi network data (WiFi name and password) and the URL addresses for the robot's requests.

Before running this program, make sure to install the required Arduino libraries from the library manager in the Arduino IDE.


The code includes libraries like WiFi, HTTPClient, and Serial, which should be installed.

Replace "YOUR WiFi Name" with your WiFi network name and "WiFi Password" with your network's password. Additionally, modify the URL addresses for the GET requests based on your robot's needs.

The code repeatedly calls the server and executes commands with a specified time interval (5 seconds), and you can adjust this time interval if necessary.

One example of running this program is to place it in a robot control unit connected to the internet, where the server can be called from any internet-connected device to send commands to the robot to control its movements and make specific decisions.
