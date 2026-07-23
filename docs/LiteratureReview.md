# Literature Review

## Overview

The development of intelligent public transportation systems has led to extensive research in Bluetooth Low Energy (BLE), indoor localization, Internet of Things (IoT), and automated fare collection technologies. Modern transportation networks require fast, reliable, and contactless passenger verification methods to reduce congestion, improve operational efficiency, and enhance passenger experience.

This literature review examines recent research related to BLE-based localization, automated ticket validation, indoor positioning, and secure digital fare collection. The insights obtained from these studies form the technical foundation of the proposed **Smart Transit Ticketing System Using Bluetooth Low Energy (BLE) Tags**.

---

## 1. BLE-Based Indoor Localization

### Paper

**BLE-Based Indoor Localization: Analysis of Some Solutions for Performance Improvement**

- **Authors:** Filippo Milano, Helbert da Rocha, Marco Laracca, Luigi Ferrigno, António Espírito Santo, José Salvado, Vincenzo Paciello
- **Publisher:** MDPI (Sensors)
- **Year:** 2024

### Summary

This paper investigates techniques for improving the accuracy of BLE-based indoor localization systems. The authors evaluate several approaches for reducing localization errors caused by signal fluctuations, including:

- RSSI filtering
- Multi-channel communication
- Signal processing techniques
- Performance optimization methods

The study demonstrates that appropriate filtering significantly improves localization accuracy in indoor environments.

### Relevance to the Project

The proposed railway ticketing system relies on BLE signals to identify passengers approaching smart gates and coach entrances. RSSI filtering techniques discussed in this paper can be applied to reduce false detections caused by overlapping signals from nearby platforms or adjacent railway tracks.

---

## 2. In-Vehicle Localization System for BLE Enabled Devices

### Paper

**In-Vehicle Localization System for BLE Enabled Devices**

- **Authors:** Omar A. Ammar, Mohamed H. Farouk, Amr A. Abdelghani, Youssef M. Ahmed, Youssef S. Mohamed, Azza M. Anis
- **Publisher:** International Journal of Computer Applications (IJCA)
- **Year:** 2024

### Summary

This research presents a BLE-based localization system designed specifically for vehicle environments. The authors combine BLE signal strength measurements (RSSI) with Kalman filtering to determine the location of passengers inside vehicles.

The proposed approach minimizes signal fluctuations and provides stable localization despite the confined environment.

### Relevance to the Project

A railway coach is similar to a vehicle cabin. The localization techniques presented in this paper can be adapted to determine whether a passenger has successfully entered or exited a coach, enabling automatic boarding verification without manual intervention.

---

## 3. An Intelligent Indoor Positioning Algorithm Based on Wi-Fi and Bluetooth Low Energy

### Paper

**An Intelligent Indoor Positioning Algorithm Based on Wi-Fi and Bluetooth Low Energy**

- **Authors:** Karamat Beigi, Hamed Shah-Mansouri
- **Publisher:** arXiv
- **Year:** 2023

### Summary

This paper proposes an indoor positioning system that combines Wi-Fi, BLE, and machine learning algorithms to improve positioning accuracy.

The authors demonstrate that combining multiple wireless technologies significantly improves localization performance, especially in crowded indoor environments.

### Relevance to the Project

Although the proposed project primarily uses BLE rather than Wi-Fi, this research highlights advanced positioning techniques that could improve passenger detection accuracy in busy railway stations.

Future versions of the project could integrate additional positioning technologies to further increase reliability.

---

## 4. Transit Fare Collection System: Blockchain-Assisted Payments System for Public Transport

### Paper

**Transit Fare Collection System: Blockchain-Assisted Payments System for Public Transport**

- **Author:** Aakaash Singh Chauhan
- **Publisher:** Cambridge Open Engage
- **Year:** 2025

### Summary

This work proposes a blockchain-based digital fare collection architecture for public transportation. The system emphasizes:

- Secure payment processing
- Transparent transaction records
- Digital ticket management
- Automated fare settlement

Blockchain technology ensures that ticket records remain secure and tamper-resistant.

### Relevance to the Project

Although blockchain is outside the scope of the present work, the concepts of secure digital ticket management and automated fare recording provide useful insights for future improvements of the proposed BLE-based railway ticketing system.

---

# Research Gap

Existing literature primarily focuses on improving BLE localization accuracy or secure fare collection individually. However, few studies integrate these technologies into a complete railway passenger management system.

The following limitations are observed:

- BLE localization research focuses mainly on positioning accuracy rather than railway ticket verification.
- Existing systems rarely combine automated passenger verification with physical smart gate control.
- Most digital ticketing systems still depend on manual validation by railway staff.
- Real-time coach occupancy monitoring is largely absent from current BLE-based ticketing solutions.
- Limited research integrates BLE localization, IoT hardware, backend verification, and live monitoring into a unified railway platform.

---

# Proposed Contribution

The proposed **Smart Transit Ticketing System Using Bluetooth Low Energy (BLE) Tags** addresses these research gaps by integrating:

- BLE-based passenger identification
- RSSI-based proximity estimation
- ESP32-based smart gate controllers
- Servo-operated automated entry gates
- IR sensor-based passenger confirmation
- Centralized ticket validation server
- Real-time coach occupancy monitoring
- Live dashboard for railway authorities and TTEs

Unlike previous studies that address only localization or fare collection, the proposed system combines passenger identification, automated gate control, ticket verification, occupancy tracking, and administrative monitoring into a single IoT-enabled railway management solution.

---

# Conclusion

The reviewed literature demonstrates that BLE technology provides a reliable foundation for contactless passenger identification and indoor localization. Advances in RSSI filtering, localization algorithms, and secure digital fare management provide valuable guidance for the development of an automated railway ticketing system.

Building upon these existing technologies, the proposed project introduces an integrated BLE-based smart transit solution that combines automated ticket verification, intelligent gate access, and real-time occupancy monitoring, making it a practical step toward modernizing railway passenger management.
