# Keyboard-Controlled-UAV-Navigation-and-Autonomous-Landing-Using-Real-Time-Color-Detection
![image](https://github.com/user-attachments/assets/1f40069c-634b-44d7-96f7-7ffb9487d282)

## Project Overview
Unmanned Aerial Vehicles (UAVs) are widely used for surveillance, automation, and smart navigation. This project integrates keyboard-based flight control with real-time color detection, enabling the Parrot Mambo drone to hover over colored blocks (Red, Green, Blue, or Yellow) and land autonomously upon detection.
The project leverages MATLAB and Simulink for image processing, thresholding, and drone control, making it accessible for researchers, students, and hobbyists interested in UAV-based automation.

## Objectives
- Enable manual navigation of the drone using keyboard commands.
- Implement a **real-time image processing system** using Simulink and MATLAB.
- Detect predefined colors (Red, Green, Blue, Yellow) and trigger the landing sequence.
- Ensure smooth drone operation and accurate color recognition with minimal response time.

## Tools & Technologies
- **Hardware:** Parrot Mambo Minidrone
- **Software:**
  - MATLAB & Simulink
  - Simulink Support Package for Parrot Minidrones
  - MATLAB Image Processing Toolbox
 
## Getting Started 
### Installing Dependencies**

1. Install the Parrot Minidrone Support Package:
   ```matlab
   supportPackageInstaller
   ```
2. Install Bluetooth drivers for Windows: [Install Bluetooth Drivers](https://www.mathworks.com/help/simulink/supportpkg/parrot_ug/install-windows-bluetooth-drivers.html)
3. Verify the connection by running:
   ```matlab
   openExample('parrot/GettingStartedWithVisionOnPARROTExample')
   ```
## 🔧 Project Setup
---

### **Simulink Model Setup**

- Open Simulink and select **Code Generation Template for Image Processing and Control**.
- Configure the flight control system and image processing blocks.
- Execute the following to explore a pre-built vision example:
  ```matlab
  openExample('parrot/GettingStartedWithVisionOnPARROTExample')
  ```
![image](https://github.com/user-attachments/assets/2bf63e6d-64f2-4011-a058-d0eee61bb5b8)


### **Color Detection Algorithm**

- Use **MATLAB’s Color Thresholding App** to define threshold values.
- Export these values into the Simulink image processing block.
- Implement **morphological operations** to enhance detection accuracy.

![image](https://github.com/user-attachments/assets/766f0559-dbfd-41c0-9878-241957d4dedf)
![image](https://github.com/user-attachments/assets/c70879d1-d901-448e-8710-c276772d9a1e)

### **Keyboard Flight Control Logic**

- Open the keyboard control example:
  ```matlab
  openExample('parrot/PathPlanningUsingParrotMinidroneExample')
  ```
- In the Simulink model, navigate to the Flight Control System > Path Planning subsystem. You can view (Figure 8) the Keyboard Control Logic subsystem already defined in the example.
- Controls:
  - X-Axis: ‘w’ to move forward and ‘s’ to move backward 
  - Y-Axis: ‘a’ for left and ‘d’ for right 
  - Z-Axis (Altitude): ‘v’ to ascend and ‘b’ to descend
  - Yaw: ‘g’ for clockwise and ‘h’ for anticlockwise rotations
    
![image](https://github.com/user-attachments/assets/e4241c5b-6ff3-4ff8-a622-1e3c2275e4e6)


### **Integrating Color Detection with Flight Control**

- Modify the **Landing Enable Block** in the Simulink **Path Planning Subsystem**.
- Add **image processing output** to trigger landing when the designated color is detected.

![image](https://github.com/user-attachments/assets/50e2649b-8725-4103-9bf7-90a113c94000)

---
## Deployment & Execution
### **Uploading to Drone**

1. Open the **Flight Control System Model** as a **Top Model** in Simulink.
2. Under **Hardware Settings**, select **Parrot Mambo**.
3. Click **Build, Deploy & Start** to run the model.
4. Navigate the drone manually using the keyboard.
5. Once over a colored block, the drone will detect it and land smoothly.

### **Troubleshooting**
- If the drone does not respond, check Bluetooth connectivity.
- If detection is inconsistent, re-calibrate thresholding parameters.

---

## Results 
- **Accurate Color Detection**: The system successfully detected colors under stable lighting.
- **Minimal Lag**: Real-time processing was efficient with negligible delay.
- **Smooth Landing**: The drone executed a controlled descent upon detecting the target color.
- **Stable Flight Control**: Keyboard-based navigation provided precise control.

![image](https://github.com/user-attachments/assets/89e4a385-01f4-4c4a-86c3-752bb102f08b)

---

## 📌 Future Enhancements
- Implement **adaptive thresholding** for dynamic lighting conditions.
- Explore **deep learning-based color recognition** for improved accuracy.
- Introduce **multi-color recognition** to perform additional automated tasks.
---

## Conclusion

This project successfully demonstrated **keyboard-controlled UAV navigation** with **real-time color detection and automated landing**. The integration of MATLAB-based image processing with Simulink control enabled seamless operation. The system is effective for basic automation, but further refinements can enhance adaptability in dynamic environments. Future extensions could incorporate **deep learning-based object detection** for more robust performance.

---
## Documentation & Final Video 

- [Document](https://github.com/ChinmayAmrutkar/Keyboard-Controlled-UAV-Navigation-and-Autonomous-Landing-Using-Real-Time-Color-Detection/blob/main/Keyboard-Controlled%20UAV%20Navigation%20%26%20Autonomous%20Landing.pdf)
- [Video](https://github.com/ChinmayAmrutkar/Keyboard-Controlled-UAV-Navigation-and-Autonomous-Landing-Using-Real-Time-Color-Detection/blob/main/video.mp4)
---

## References

1. [Install Bluetooth Drivers](https://www.mathworks.com/help/simulink/supportpkg/parrot_ug/install-windows-bluetooth-drivers.html)
2. [Getting Started with Parrot Minidrones](https://www.mathworks.com/help/supportpkg/parrot/ref/getting-started-with-simulink-support-package-for-parrot-minidrones.html)
3. [External Mode for Parrot Minidrones](https://www.mathworks.com/help/supportpkg/parrot/ref/external-mode-for-parrot-minidrones.html)
4. [Path Planning using Keyboard Control](https://www.mathworks.com/help/simulink/supportpkg/parrot_ref/path-planning-keyboard-example.html)
5. [MATLAB example om Path Planning Using Keyboard Control for Parrot Minidrone](https://www.mathworks.com/help/simulink/supportpkg/parrot_ref/path-planning-keyboard-example.html)
---



