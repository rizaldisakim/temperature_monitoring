# temperature_monitoring
Individual Development Project as part of Enrichhment Program, focusing on fryer area temperature monitoring between LH3 and LH4

## 🛠️ Tech Stack & Architecture

Project ini dibangun menggunakan infrastruktur berbasis *baremetal* langsung di atas OS Ubuntu Desktop pada perangkat Edge Gateway (Raspberry Pi), dengan rincian *tech stack* sebagai berikut:

| Layer | Teknologi / Tools | Deskripsi |
| :--- | :--- | :--- |
| **Hardware / Sensors** | `Zigbee Sensors` | Sensor nirkabel untuk mendeteksi suhu & kelembaban di area mesin fryer. |
| **Edge Gateway OS** | `Ubuntu Server` | Sistem Operasi utama tempat seluruh service berjalan native di latar belakang. |
| **Ingestion Layer** | `Zigbee2MQTT` | Menerjemahkan sinyal nirkabel Zigbee menjadi payload data JSON via serial dongle. |
| **Processing Layer** | `Node-RED` | *Data broker* untuk memproses payload, memfilter duplikasi, dan mengarahkan alur data. |
| **Storage Layer** | `InfluxDB` | *Time-Series Database* untuk menampung data historis secara efisien. |
| **Visualization Layer** | `Grafana` | Dashboard visualisasi real-time untuk memantau tren suhu bulanan dan LQI sinyal. |
| **Alerting Layer** | `Slack` | Integrasi *Incoming Webhooks* untuk mengirimkan notifikasi otomatis saat terjadi suhu ekstrem. |

### 🚀 Badges
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![Zigbee](https://img.shields.io/badge/Zigbee-EB212E?style=for-the-badge&logo=zigbee&logoColor=white)
![MQTT](https://img.shields.io/badge/MQTT-660066?style=for-the-badge&logo=mqtt&logoColor=white)
![Node-RED](https://img.shields.io/badge/Node--RED-8F0000?style=for-the-badge&logo=node-red&logoColor=white)
![InfluxDB](https://img.shields.io/badge/InfluxDB-22ADF6?style=for-the-badge&logo=influxdb&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![Slack](https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white)
