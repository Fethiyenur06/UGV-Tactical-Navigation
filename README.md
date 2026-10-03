# UGV Tactical Navigation (GPS-Denied)

## Overview
This repository contains a C++ implementation of a robust sensor fusion algorithm designed for Unmanned Ground Vehicles (UGVs). The primary objective is to maintain accurate orientation and navigation telemetry in environments where GPS signals are jammed or compromised (GPS-denied environments).

## Architecture
The system integrates an MPU6050 (6-DOF IMU) utilizing a custom Extended Kalman/Complementary Filter structure to output clean Pitch, Roll, and Yaw estimations. 
It is optimized for real-time embedded systems (STM32, Nuvoton, Raspberry Pi) with strict loop-time constraints (100Hz).

### Key Features:
- **Sensor Fusion:** Combines raw accelerometer and gyroscope data to eliminate high-frequency mechanical vibration noise.
- **Embedded-Ready:** Lightweight C++ architecture easily adaptable to RTOS (Real-Time Operating System) environments.
- **Harsh Terrain Tuning:** Filter coefficients are structured to handle the dynamic instability of off-road ground vehicles.

## Future Implementation
- Integration with LiDAR SLAM for complete autonomous mapping.
- Adding PID-based motor command outputs derived from the current yaw estimate.
