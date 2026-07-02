# Krysalis Hand Case Study

Public-safe case study of embedded firmware and electronics debugging work for Krysalis Hand, a humanoid robotic hand research platform developed in the Laboratory for AI, Robotics and Automation (LARA) at UC Davis.

> Note: This repository is a public-facing case study. It does not include private lab source code, unreleased CAD, PCB files, internal documentation, or confidential test data.

## Overview

Krysalis Hand is a dexterous robotic hand platform used for robotics research and experimentation with real hardware. My work has focused on the firmware and electronics layer: stabilizing communication between distributed embedded components, debugging I2C behavior, and supporting PCB-level improvements that make the system more reliable.

This project sits at the intersection of embedded firmware, electronics debugging, PCB design, and robotics integration.

## My Role

Undergraduate Student Researcher, Laboratory for AI, Robotics and Automation (LARA)

Focus areas:

- Embedded firmware debugging
- Hardware/software integration
- I2C communication reliability
- PCB-level electronics improvements
- ROS2/micro-ROS integration support

## Technical Problem

Robotic hands require reliable low-latency communication across many embedded components. When command, sensor, or actuator signals are unreliable, the issue can live at several layers:

- Firmware message handling
- I2C bus timing and contention
- Pull-up resistor selection
- Voltage regulation and signal integrity
- Inbound/outbound command routing
- Interface behavior between embedded firmware and robotics software

The practical challenge was not just writing code. It was isolating failure modes across firmware, electronics, and the physical robot.

## System Context

```mermaid
flowchart LR
    A[ROS2 / micro-ROS control pipeline] --> B[Embedded firmware]
    B --> C[I2C communication bus]
    C --> D[Distributed hand electronics]
    D --> E[Motors / sensors / hand mechanisms]
    D --> B
```

## Contributions

### I2C Bus Debugging

Investigated bus contention and communication reliability issues across distributed embedded components. The goal was to identify where communication failures originated and improve the consistency of command and sensor data flow.

Key work:

- Traced communication behavior across firmware and hardware boundaries
- Diagnosed I2C bus contention symptoms
- Helped stabilize low-latency communication on real hardware

### Firmware Signal Path Improvements

Worked on inbound and outbound signal paths so commands and hardware responses could move through the system more reliably.

Key work:

- Reworked command/data routing logic
- Improved separation between inbound and outbound communication paths
- Supported more predictable firmware behavior during hardware testing

### PCB-Level Hardware Improvements

Supported electronics hardening work related to signal integrity and power stability.

Key work:

- Evaluated pull-up resistor behavior for I2C reliability
- Contributed to voltage-regulation improvements
- Helped connect observed firmware issues to board-level design choices

### Robotics Integration

Connected embedded-system debugging work to the broader robotics stack used on the platform.

Key work:

- Worked within ROS2/micro-ROS integration requirements
- Debugged behavior on physical hardware rather than isolated simulation
- Focused on reliability at the firmware/electronics/robotics boundary

## Skills Demonstrated

- Embedded systems
- Firmware debugging
- I2C communication
- PCB design and electronics debugging
- Microcontrollers
- Hardware/software integration
- ROS2 and micro-ROS
- Real-hardware robotics testing

## Results

This work improved the reliability of the embedded communication path and helped move the robotic hand toward more stable operation during testing.

Public-safe summary:

- Diagnosed communication problems across firmware and electronics layers
- Improved reliability of inbound/outbound signal handling
- Supported PCB-level improvements involving pull-ups and voltage regulation
- Practiced debugging on real robotic hardware under system-level constraints

## What I Learned

- Real embedded debugging is usually cross-layer: firmware symptoms often point to electrical or board-level causes.
- I2C reliability depends heavily on bus topology, pull-ups, timing, and the behavior of every device on the bus.
- Robotics firmware has to be evaluated on physical hardware because timing and integration issues often do not appear in isolated tests.
- Clear signal paths make embedded systems easier to test, debug, and extend.

## Repository Status

Current status: public case study

Planned additions:

- Sanitized block diagrams
- Public-safe timing notes
- Photos or diagrams cleared for public release
- Short demo walkthrough video

## Related Links

- GitHub profile: https://github.com/vadimfedorovsv
- LinkedIn: https://www.linkedin.com/in/vadim-fedorov-sv/
