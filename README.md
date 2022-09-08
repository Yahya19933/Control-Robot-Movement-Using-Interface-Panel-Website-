# Control-Robot-Movement-Using-Interface-Panel-Website-
Design an interface to control the movement of the robot which could be in (forward, left, backward, right)

Design an interface to control the movement of the robot which could be in (forward, left, backward, right) direction. When user click on a certain direction the movement will be stored in a database

![Capture](https://user-images.githubusercontent.com/90250848/189161097-7158cf1e-eefd-4400-b449-2239b79d1279.PNG)



## Pre-requisites
 To be able to send and get data from MYSQL database we have to install MYSQL database, you can use [XAMPP](https://www.apachefriends.org/) which i an open-source cross-platform web server
 
 ## Explanation Steps
 1. After installing XAMPP create a folder named "movement" in xampp path *xampp>htdocs*
 
 2. Copy the two files attched above, sendMovementValues and getMovement.php to movement folder
 

4. Before uploading the code **Movement.ino** , make sure to change the **ssid** and **password** to your WiFi. After uploding the code will read the data from the database frequently using GET method

5.In **phpMyAdmin**, create a database named "esp32", then create a table named "movement" with values shown in below image

![movement_db](https://user-images.githubusercontent.com/90250848/189160248-e6c97409-0692-409f-9f14-edc4ab140f9f.jpg)


6. When the user click the forward button, the website will send "forward" to the database and ESP32 will read it to move forward, and when the user click the right button, we will send "right" to the database and ESP32 will also turn right

As you see in the image above, we also register how long did the user pressed the button, he clicked the forward button for 3.3 seconds and clicked the right button for 1.6 seconds. This is useful later if we want the robot replay what the user clickd before

![Capture](https://user-images.githubusercontent.com/90250848/189160773-672b7a44-dda3-41cd-8477-c6512c89ad94.PNG)

