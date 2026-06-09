## Temperature Monitoring
Individual Development Project as part of Enrichhment Program, focusing on fryer area temperature monitoring between LH3 and LH4

## Key-Technology Stack & Architecture
This project is built using a baremetal infrastructure running directly on top of the Ubuntu Desktop operating system on an Edge Gateway device (Raspberry Pi 5). The detailed tech stack is structured as follows:

| Layer | Technology / Tools | Description |
| :--- | :--- | :--- |
| **Hardware / Sensor** | `Zigbee Temperature and Humidity Sensor, Model SNZB-02P` | Wireless sensors deployed to detect temperature & humidity variations in the fryer machine area. |
| **Hardware / Gateway** | `Zigbee 3.0 USB Dongle Plus, Model ZBDongle-E` | Physical coordinator hardware configured with custom firmware to manage the wireless mesh network and capture sensor data. |
| **Edge Gateway OS** | `Ubuntu Desktop` | The primary operating system, where all core technologies/services run natively in the background. |
| **Ingestion Layer** | `Zigbee2MQTT` | Bridges the wireless Zigbee signals into structured JSON data payloads via a serial USB dongle. |
| **Processing Layer** | `Node-RED` | Acts as the data broker to ingest payloads, filter out duplications, and direct the data pipeline. |
| **Storage Layer** | `InfluxDB` | A Time-Series Database optimized for efficiently handling high-frequency historical telemetry data. |
| **Visualization Layer** | `Grafana` | Real-time visualization dashboard used to monitor monthly temperature trends and signal quality (LQI). |
| **Alerting Layer** | `Slack` | Integrated via Incoming Webhooks to dispatch instant automated notifications whenever extreme temperature anomalies occur. |

## Badges
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![Zigbee](https://img.shields.io/badge/Zigbee-EB212E?style=for-the-badge&logo=zigbee&logoColor=white)
![MQTT](https://img.shields.io/badge/MQTT-660066?style=for-the-badge&logo=mqtt&logoColor=white)
![Node-RED](https://img.shields.io/badge/Node--RED-8F0000?style=for-the-badge&logo=node-red&logoColor=white)
![InfluxDB](https://img.shields.io/badge/InfluxDB-22ADF6?style=for-the-badge&logo=influxdb&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![Slack](https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white)
