
# 3D Shape Display with MPU6050 and OLED (for ESP32)

This project uses an **ESP32** board, an **MPU6050 accelerometer/gyro sensor**, and an **OLED display** to show a rotating 3D shape (cube or pyramid) based on the device's orientation. The accelerometer data (x, y, z values) is also displayed on the screen, and you can switch between different shapes using a button.

## Features

- **Rotating 3D Shapes**: A cube or pyramid that rotates .
- **Real-time Data**: Shows the x, y, and z values from the MPU6050 sensor.
- **Interactive Button**: Press a button to switch between a cube and pyramid.
- **Graphical Display**: Shows a plot of the accelerometer data on the OLED screen.

## Hardware Needed

- **ESP32** board
- **MPU6050** accelerometer/gyro sensor
- **OLED display (128x64)**
- **Button** (for toggling between cube and pyramid)

## Wiring

1. **MPU6050**:
   - VCC -> 3.3V or 5V (depends on your ESP32)
   - GND -> GND
   - SDA -> GPIO 21 (default for ESP32)
   - SCL -> GPIO 22 (default for ESP32)

2. **OLED Display**:
   - VCC -> 3.3V or 5V
   - GND -> GND
   - SDA -> GPIO 21
   - SCL -> GPIO 22

3. **Button**:
   - One pin -> GPIO 4
   - Other pin -> GND

## Software Requirements

1. **Arduino IDE** (Download from [here](https://www.arduino.cc/en/software))
2. **Libraries**:
   - `Wire` (for I2C communication)
   - `Adafruit_GFX` (for graphics)
   - `Adafruit_SSD1306` (for OLED display)
   - `Adafruit_MPU6050` (for MPU6050 sensor)

You can install these libraries from the Arduino IDE's Library Manager.

2. **Install Libraries**:
   - Open Arduino IDE, go to **Sketch > Include Library > Manage Libraries**.
   - Search for and install:
     - **Wire**
     - **Adafruit GFX**
     - **Adafruit SSD1306**
     - **Adafruit MPU6050**

3. **Upload the Code**:
   - Open the file in the Arduino IDE.
   - Choose your **ESP32 board** and **port** from **Tools > Board** and **Tools > Port**.
   - Click **Upload** to upload the code to your ESP32.

## How to Use

- Once the program starts, you'll see a rotating 3D shape (either a cube or pyramid).
- Press the button to switch between the cube and pyramid.
- The accelerometer's x, y, and z data will be displayed on the screen.
- As you tilt your ESP32, the shape will rotate based on the orientation of the device.
