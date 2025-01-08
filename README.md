# Engineering & Technical Experience Portfolio
## Yi Li

## Embedded Systems Development

### Space Invaders Game System
**Technologies:** Arduino Uno, C++, LED Matrix Display, Sensors
**Duration:** Fall 2023

**System Architecture:**
- Microcontroller: Arduino Uno
- Input Devices: Potentiometer for movement control, Push button for action trigger
- Display: 16x32 RGB LED Matrix Panel
- Interface: Custom-designed breadboard circuit

**Technical Implementation:**
```cpp
// Example of sensor data processing with smoothing
class InputController {
private:
    const int POT_PIN = A5;
    const int BUTTON_PIN = 10;
    float currentPosition = 0;
    
public:
    void updatePosition() {
        // Read and process potentiometer input with smoothing
        int rawValue = analogRead(POT_PIN);
        float targetPosition = map(rawValue, 0, 1023, 0, SCREEN_WIDTH);
        currentPosition = (currentPosition * 0.7) + (targetPosition * 0.3);
    }
};
```

**Key Technical Achievements:**
1. Sensor Integration
   - Implemented real-time potentiometer reading with data smoothing
   - Developed debouncing solution for button input
   - Created efficient polling system for input devices

2. Display System
   - Engineered refresh rate optimization for smooth animation
   - Implemented efficient sprite rendering system
   - Managed memory constraints for display buffer

3. Circuit Design
   - Created complete circuit integration on breadboard
   - Implemented proper power distribution
   - Managed ground connections for multiple components

## Industrial Automation Experience

### Robotics Data Acquisition System at Paslin
**Technologies:** C++, Siemens Process Simulate, Teamcenter
**Duration:** Summer 2024

**System Overview:**
- Developed data collection system for manufacturing robots
- Implemented safety parameter verification
- Created cross-platform data conversion utilities

**Technical Implementation:**
```cpp
// Example of robot data processing system
class RobotDataProcessor {
    struct SafetyMetrics {
        double speedLimit;
        Vector3D workspaceBoundary;
        bool collisionDetected;
    };
    
    void processRobotData(const RobotData& data) {
        // Safety checks and data validation
        SafetyMetrics metrics = validateSafetyParameters(data);
        
        // Process and store validated data
        if (metrics.collisionDetected) {
            triggerSafetyAlert();
        }
    }
};
```

**Key Achievements:**
1. Data Collection System
   - Real-time metric collection from robot controllers
   - Automated safety parameter verification
   - Integration with Siemens Process Simulate

2. Safety System Implementation
   - Workspace boundary verification
   - Speed limitation monitoring
   - Collision detection algorithms

## Additional Technical Projects

### EECSGPT: Course Syllabus Assistant
**Technologies:** Python, NLP, SQL
- Developed AI-powered document retrieval system
- Implemented vectorized text processing
- Created efficient query processing pipeline

### Food Recipe Analysis Platform
**Technologies:** Python, Data Analysis, Web Development
- Led development of data analysis system
- Implemented machine learning models
- Created interactive data visualization dashboard

## Technical Skills Summary

1. Programming Languages
   - C/C++ (Embedded & System Programming)
   - Python (Data Processing & Analysis)
   - Java (Application Development)

2. Hardware & Embedded Systems
   - Arduino Platform
   - Sensor Integration
   - Circuit Design
   - Real-time Systems

3. Industrial Tools
   - Siemens Process Simulate
   - Teamcenter
   - Version Control (Git)

4. Data Processing
   - Real-time Data Collection
   - Signal Processing
   - Statistical Analysis
