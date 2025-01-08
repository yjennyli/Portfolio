# Engineering & Technical Experience Portfolio
## Yi Li

## Embedded Systems Development

### Space Invaders Game System
**Technologies:** Arduino Uno, C++, LED Matrix Display, Sensors
**Duration:** September 2023 - January 2024

**System Architecture:**
- Microcontroller: Arduino Uno
- Input Devices: 
  - Potentiometer (Analog Pin 5) for player movement
  - Push button (Digital Pin 10) for firing control
- Display: Adafruit 16x32 RGB Matrix Panel
  - CLK, LAT, OE pins for timing control
  - RGB color management using Color333 system
- Interface: Custom breadboard circuit integration

**Core Implementation Details:**
```cpp
// Color Management System
class Color {
public:
    int red, green, blue;
    Color(int r, int g, int b) {
        red = r;
        green = g;
        blue = b;
    }
    uint16_t to_333() const {
        return matrix.Color333(red, green, blue);
    }
};

// Game Object System
class Game {
private:
    int level;
    unsigned long time;
    Player player;
    Cannonball ball;
    Invader enemies[NUM_ENEMIES];
    
public:
    void update(int potentiometer_value, bool button_pressed) {
        // Real-time game state updates
        // Input processing and display refresh
    }
};

// Main Control Loop
void loop() {
    int potentiometer_value = analogRead(POTENTIOMETER_PIN_NUMBER);
    bool button_pressed = (digitalRead(BUTTON_PIN_NUMBER) == HIGH);
    game.update(potentiometer_value, button_pressed);
}
```

**Technical Implementation Highlights:**
1. Object-Oriented Design
   - Implemented distinct classes for Game, Player, Invader, and Cannonball
   - Created robust Color management system for RGB LED control
   - Developed modular system architecture for maintainability

2. Hardware Integration
   - Configured multiple GPIO pins for LED matrix control
   - Implemented analog input processing for smooth player movement
   - Managed display refresh timing for optimal performance

3. Real-time Processing
   - Developed efficient game loop with consistent update cycles
   - Implemented input smoothing for precise control
   - Optimized display updates for fluid animation

## Industrial Automation Experience

### Robotics Data Acquisition System at Paslin
**Technologies:** Python, Siemens Process Simulate, Teamcenter
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
