# Thermometer-Simulation
# Thermometer Simulation

Here's a complete working implementation of a thermometer simulation using HTML/JavaScript (for the frontend), C++ (for a backend simulation), and Java (for a middle layer). This is a multi-part implementation that simulates how a thermometer might work across different technology stacks.


      

## How to Run This System

1. *C++ Sensor Program*:
   - Compile with: g++ thermometer_sensor.cpp -o thermometer_sensor -std=c++11 -pthread
   - Run with: ./thermometer_sensor

2. *Java Middleware*:
   - Compile with: javac ThermometerServer.java
   - Run with: java ThermometerServer
   - Note: This uses the com.sun.net.httpserver package which is included in the JDK

3. *HTML/JavaScript Frontend*:
   - Save the HTML code to a file (e.g., thermometer.html)
   - Open it in a web browser
   - For a complete system, modify the JavaScript to fetch temperature from the Java server (http://localhost:8000/temperature) instead of using the simulated values

## How It Works

1. *C++ Program*:
   - Simulates a physical thermometer with random temperature fluctuations
   - Outputs the current temperature to stdout every second
   - Represents the "hardware" layer of the thermometer

2. *Java Program*:
   - Reads the temperature values from the C++ program's output
   - Provides a REST API endpoint (/temperature) that returns the current temperature in JSON format
   - Acts as middleware between the hardware and the web interface

3. *HTML/JavaScript*:
   - Displays a visual thermometer with a mercury level
   - Shows the current temperature in Celsius or Fahrenheit
   - In a full implementation, would fetch data from the Java server

This implementation demonstrates how a thermometer system might be built across different technology stacks, with each component handling a specific responsibility.
