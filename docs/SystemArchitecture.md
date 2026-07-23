# System Architecture

## Project Title

**Smart BLE-Based Railway Ticketing and Automated Boarding System**

---

# 1. Overview

The Smart BLE-Based Railway Ticketing and Automated Boarding System is a distributed Internet of Things (IoT) architecture that integrates embedded hardware, wireless communication, cloud services, and web applications to automate passenger verification and railway boarding.

The system consists of five primary layers:

1. Passenger Layer
2. Smart Gate Layer
3. Communication Layer
4. Backend Layer
5. User Interface Layer

Together, these layers provide seamless passenger identification, ticket verification, automated gate control, and real-time operational monitoring.

---

# 2. High-Level Architecture

```text
                         +----------------------+
                         |  Passenger Credential |
                         | (BLE Tag / Mobile App)|
                         +----------+-----------+
                                    |
                             BLE Advertisement
                                    |
                                    ▼
                    +-------------------------------+
                    | Smart Gate (ESP32 Controller) |
                    | - BLE Scanner                 |
                    | - Servo Motor                 |
                    | - IR/Ultrasonic Sensor        |
                    | - LED & Buzzer                |
                    +---------------+---------------+
                                    |
                               Wi-Fi / MQTT / HTTP
                                    |
                                    ▼
                     +------------------------------+
                     |        Backend Server        |
                     |------------------------------|
                     | Authentication               |
                     | Ticket Verification          |
                     | Boarding Logic               |
                     | Event Logging                |
                     | Occupancy Engine             |
                     +---------------+--------------+
                                     |
                     +---------------+---------------+
                     |                               |
                     ▼                               ▼
              PostgreSQL / Firebase          REST API
                     |                               |
                     ▼                               ▼
          Admin Dashboard                 TTE Dashboard
```

---

# 3. System Components

## 3.1 Passenger Layer

The passenger carries a registered BLE-enabled credential that broadcasts a unique identifier.

Possible credentials include:

* BLE tag
* BLE keychain
* BLE wristband
* Mobile application (future work)

The BLE identifier is associated with a passenger account and ticket information in the backend database.

---

## 3.2 Smart Gate Layer

The smart gate is responsible for:

* Detecting BLE devices.
* Measuring signal strength (RSSI).
* Confirming physical presence using proximity sensors.
* Sending verification requests to the backend.
* Opening or closing the gate.
* Logging entry events.

### Hardware Components

* ESP32
* Servo motor
* Ultrasonic or IR sensor
* RGB LED
* Buzzer
* OLED Display (optional)

---

## 3.3 Communication Layer

Communication between hardware and the backend occurs through Wi-Fi.

Possible protocols include:

* HTTP REST API
* MQTT
* WebSocket (future enhancement)

The gate transmits:

* Gate ID
* BLE Identifier
* Timestamp
* Signal strength
* Sensor status

to the backend server.

---

## 3.4 Backend Layer

The backend is the central decision-making component.

Responsibilities include:

* Passenger authentication
* Ticket verification
* Journey validation
* Duplicate entry prevention
* Boarding event logging
* Occupancy calculation
* Alert generation

### Verification Checks

* Is the BLE credential registered?
* Is there a valid ticket?
* Is the journey scheduled for today?
* Is the passenger at the correct station?
* Has the passenger already entered?
* Is access authorized?

---

## 3.5 Database Layer

The database stores:

### Passenger Information

* Passenger ID
* Name
* Registered BLE Identifier

### Ticket Information

* PNR
* Train Number
* Coach
* Seat
* Journey Date

### Entry Logs

* Entry Time
* Gate Number
* Verification Status
* Boarding Status

### System Logs

* Alerts
* Errors
* Security Events

---

## 3.6 Dashboard Layer

### Administrator Dashboard

Displays:

* Gate status
* Passenger entries
* Boarding statistics
* Coach occupancy
* Alerts
* System health

### TTE Dashboard

Displays:

* Passenger verification status
* Boarding confirmation
* Seat information
* Coach assignment
* Unverified passengers

---

# 4. Operational Workflow

The following sequence illustrates the overall operation of the system:

1. Passenger books a railway ticket.
2. The ticket is associated with a registered BLE credential.
3. The passenger approaches the smart gate.
4. The ESP32 detects the BLE advertisement.
5. The proximity sensor confirms the passenger is at the gate.
6. The gate sends a verification request to the backend.
7. The backend validates the journey.
8. If verification succeeds:

   * The gate opens.
   * The event is logged.
   * Dashboard statistics are updated.
9. If verification fails:

   * The gate remains closed.
   * An alert is generated.

---

# 5. Security Considerations

The architecture incorporates several security mechanisms:

* Registered BLE credentials only.
* Duplicate entry detection.
* Backend-side authorization.
* Entry event logging.
* Optional encrypted BLE identifiers (future work).
* Role-based access for administrative dashboards.

---

# 6. Scalability

The architecture is designed to support future expansion by allowing:

* Multiple stations.
* Multiple smart gates.
* Additional coaches.
* Cloud deployment.
* Mobile applications.
* AI-assisted crowd analytics.
* Integration with existing railway infrastructure.

---

# 7. Design Principles

The system follows these architectural principles:

* Modular hardware design.
* Layered software architecture.
* Separation of concerns.
* Scalable backend services.
* Real-time event processing.
* Maintainability and extensibility.

---

# 8. Conclusion

The proposed architecture provides a modular and scalable framework for demonstrating BLE-assisted automated railway boarding. By integrating IoT hardware, wireless communication, backend verification, and real-time dashboards, the system serves as a proof of concept for intelligent passenger verification and operational monitoring in railway environments.
