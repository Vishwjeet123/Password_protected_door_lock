# Password_protected_door_lock

Components Needed:
1. NodeMCU ESP8266
2. Servo Motor (to control the door lock)
3. LEDs (Green and Red)
4. Buzzer
5. 4.7kΩ or 10kΩ Resistors (for pull-up/down if needed)
6. Mobile Phone or Web App (to input the password)
7. Breadboard and Wires
8. Power Supply

Step-by-Step Approach:

1. Setup the Hardware  
- Connect the servo motor to the NodeMCU (control pin to D5, power, and ground).  
- Attach the green LED to D1 and red LED to D2 (via appropriate resistors).  
- Connect the buzzer to D3.  

2. Web Server on NodeMCU  
- Create a simple web server hosted by the ESP8266 using the ESPAsyncWebServer library.  
- Use an HTML form where users can input the password.  

3. Password Handling
- Store a predefined password in the code.  
- When the user enters the password via the mobile/web app, send it to the ESP8266 server for validation.  

4. Logic for Door Operation  
- If the entered password matches:  
  - Turn the green LED ON.  
  - Move the servo motor to unlock the door.  
- If the password is incorrect:  
  - Turn the red LED ON.  
  - Activate the buzzer for a few seconds.  


Key Features:
1. Web-based Password Entry: You can access the ESP8266's server using any browser.  
2. Secure Access: The predefined password ensures security.  
3. Real-time Feedback: LEDs and buzzer provide instant feedback for the entered password.

