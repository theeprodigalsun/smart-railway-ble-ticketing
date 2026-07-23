# Project Scope

## Project Title

**Smart BLE-Based Railway Ticketing and Automated Boarding System**

## Overview

This project focuses on the design and development of a prototype smart railway boarding system that leverages Bluetooth Low Energy (BLE), Internet of Things (IoT) technologies, ESP32-based smart gates, and a centralized backend to automate passenger verification and improve the railway boarding process.

The system aims to demonstrate how wireless identification and intelligent access control can reduce manual ticket verification while providing railway authorities with real-time operational data.

---

## In Scope

The project includes the following functionalities:

### 1. BLE-Based Passenger Identification

* Detect registered BLE-enabled passenger credentials.
* Associate BLE identifiers with valid railway tickets in the backend.
* Verify passenger identity during boarding.

### 2. Smart Entry Gate

* ESP32-controlled automated gate.
* Servo-based gate operation.
* Entry authorization based on backend verification.
* Visual and audible status indicators.

### 3. Ticket Verification

The backend validates:

* Ticket validity
* Journey date
* Train number
* Boarding station
* Passenger entry status

before granting access.

### 4. Boarding Event Logging

The system records:

* Passenger entry time
* Gate used
* Boarding confirmation
* Verification status

for administrative monitoring.

### 5. Coach Occupancy Monitoring

Estimate coach occupancy using verified boarding events and present the information through an administrative dashboard.

### 6. Administrative Dashboard

Provide railway administrators with:

* Live gate status
* Passenger entry statistics
* Boarding records
* Coach occupancy information
* System alerts

### 7. TTE Dashboard

Provide Ticket Travelling Examiners (TTEs) with a simplified interface displaying:

* Passenger verification status
* Boarding confirmation
* Seat information
* Alerts for unverified passengers

### 8. Prototype Demonstration

Develop a working laboratory-scale prototype consisting of:

* BLE tags
* ESP32 smart gate
* Backend server
* Database
* Web dashboard

---

## Out of Scope

The following items are outside the scope of this project:

* Integration with the live IRCTC reservation system.
* Deployment in operational railway stations.
* Railway payment processing.
* Nationwide passenger registration.
* Production-grade cybersecurity infrastructure.
* Large-scale cloud deployment.
* Support for every smartphone and BLE device.
* Integration with existing railway signalling systems.
* Commercial ticket booking functionality.

---

## Assumptions

This project assumes that:

* Passengers possess a registered BLE-enabled credential (such as a BLE tag or supported mobile device).
* Smart gates have reliable network connectivity to communicate with the backend.
* BLE communication is supported within the prototype environment.
* The backend database contains valid passenger and ticket information.
* Prototype testing is performed under controlled conditions.

---

## Constraints

The project is subject to the following constraints:

* Limited prototype hardware budget.
* Laboratory-scale testing rather than real railway deployment.
* BLE signal variations caused by environmental conditions.
* Time constraints associated with an undergraduate final-year project.
* Limited access to proprietary railway infrastructure and APIs.

---

## Expected Deliverables

By the completion of the project, the following deliverables are expected:

* Functional ESP32-based smart gate prototype.
* BLE-based passenger identification system.
* Backend ticket verification service.
* Database for passenger and journey records.
* Administrative dashboard.
* TTE dashboard.
* Hardware design documentation.
* Software source code.
* System documentation and testing results.

---

## Future Scope

The proposed system can be extended through future research and development, including:

* Integration with official railway reservation systems.
* Mobile application support.
* AI-based crowd prediction and passenger flow analysis.
* Secure cryptographic BLE authentication.
* Multi-factor passenger verification.
* Smart platform navigation assistance.
* Digital twin simulation of station operations.
* Predictive analytics for coach occupancy and station congestion.

---

## Project Boundary

This project is intended as a **proof-of-concept prototype** that demonstrates the feasibility of BLE-assisted automated passenger verification and smart railway boarding. The emphasis is on validating the system architecture, hardware integration, software implementation, and operational workflow rather than replacing existing railway ticketing infrastructure.
