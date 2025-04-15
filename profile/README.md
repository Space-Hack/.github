# Space Hack Project

This project was created during the ARIS x Colosseum ETH Entrepreneur Club Space Hackathon 2025, where our team won the 1st round and secured 3rd place in the final. Built in just 21 hours, this system demonstrates natural language robotics control with a futuristic dashboard interface.

## Team
- [Kirill Heitzler](https://www.linkedin.com/in/kirill-heitzler/)
- [Noah Gerber](https://www.linkedin.com/in/noah-gerber-a62442229/)
- [Sebastian Truijens](https://www.linkedin.com/in/sebastian-truijens/)
- [Rui Zhang](https://www.linkedin.com/in/rui-zhang-978822290/)
- [Lukas Diebold](https://www.linkedin.com/in/lukas-diebold/)

## Project Overview
In just under a night, we built an autonomous robot that:
- Responds to natural language commands
- Performs physical actions
- Streams live video to a custom-built web interface
- Features a futuristic dashboard (mission control for a Mars colony)
- Provides telemetry data and environment monitoring
- Offers real-time robot feed

This project consists of three main components that work together to control and manage robotic systems:

## Project Structure

### 1. vex-iq-serial-control/
A VEX IQ2 Clawbot control system that implements serial communication for remote robot control. This component:
- Controls drive motors, arm, and claw operations
- Provides real-time sensor data feedback (distance, bumper state, heading)
- Implements precise motor control for various robot movements
- Uses a simple command format for remote control
- Monitors multiple sensors including distance, bumper, and inertial sensors

### 2. pythonSerial/
A Python-based WebSocket bridge that enables bidirectional communication between serial devices (VEX IQ Robot) and a WebSocket server. This component:
- Establishes real-time data transfer between serial ports and WebSocket connections
- Handles error management and graceful shutdown
- Provides thread-safe implementation for reliable communication
- Configurable for different serial ports and baud rates

### 3. RobotControlServer/
A FastAPI-based server application that serves as the central control system. This component:
- Provides REST API endpoints for robot control
- Manages WebSocket connections for real-time communication
- Integrates AI capabilities for advanced robot control
- Implements modular architecture with separate components for API, WebSocket handling, AI processing, and command parsing
- Includes a test client for development and testing

## Getting Started

Each component has its own setup and configuration requirements. Please refer to the respective directories for detailed documentation and setup instructions.

## Dependencies

- Python 3.x
- Serial communication libraries
- VEX IQ2 Brain and VEX V5 IDE (for vex-iq-serial-control)
- FastAPI and WebSocket libraries (for RobotControlServer)
- Additional dependencies specified in each component's requirements.txt
