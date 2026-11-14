# 🚀 Real-Time Server Monitoring & Alerting System

## 📌 Project Overview

The **Real-Time Server Monitoring & Alerting System** is a DevOps project designed to monitor server health and system resource utilization using Prometheus, Node Exporter, Grafana, and Alertmanager.

It collects system metrics such as CPU usage, memory utilization, disk usage, and network traffic. Grafana provides interactive dashboards, while Alertmanager handles notifications when configured thresholds are exceeded.

## 🎯 Project Objectives

- Monitor server performance in real time.
- Track CPU, memory, disk, and network utilization.
- Visualize system metrics through Grafana dashboards.
- Configure automated alerts for resource-related issues.
- Manage monitoring services using Docker Compose.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Linux (Ubuntu/WSL) | Operating environment |
| Docker | Containerization |
| Docker Compose | Container orchestration |
| Prometheus | Metrics collection and monitoring |
| Node Exporter | System metrics exporter |
| Grafana | Monitoring dashboards |
| Alertmanager | Alert management and notifications |

## 🏗️ Project Architecture

```text
              Linux / WSL Environment
                       |
                       v
                 Node Exporter
                       |
                       v
                  Prometheus
                       |
             +---------+---------+
             |                   |
             v                   v
          Grafana            Alertmanager
             |                   |
             v                   v
       Monitoring Dashboard   Email Alerts
```

## 📂 Project Structure

```text
server-monitoring/
│
├── docker-compose.yml
├── .gitignore
├── README.md
│
├── prometheus/
│   ├── prometheus.yml
│   └── alerts.yml
│
├── alertmanager/
│   └── alertmanager.example.yml
│
└── screenshots/
```

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/Nani-software/Real-Time-Server-Monitoring-Alerting-System.git
```

### 2. Navigate to the project directory

```bash
cd Real-Time-Server-Monitoring-Alerting-System
```

### 3. Start the monitoring stack

```bash
sudo docker compose up -d
```

### 4. Check running containers

```bash
sudo docker compose ps
```

## 🌐 Access Monitoring Services

| Service | Local URL |
|---|---|
| Grafana | http://localhost:3000 |
| Prometheus | http://localhost:9090 |
| Alertmanager | http://localhost:9093 |
| Node Exporter | http://localhost:9100/metrics |

## 📊 Grafana Dashboard

Configure Prometheus as a Grafana data source.

**Prometheus Data Source URL:**

```text
http://prometheus:9090
```

Import the Node Exporter Full dashboard using dashboard ID:

```text
1860
```

The dashboard can display:

- CPU utilization
- Memory usage
- Disk utilization
- Network traffic
- System performance metrics

## 🚨 Alert Configuration

Prometheus alert rules are configured in:

```text
prometheus/alerts.yml
```

Example alert conditions:

- High CPU usage above 80%.
- High memory usage above 85%.
- High disk usage above 85%.
- Node Exporter target unavailable.

Alertmanager can be configured to send email notifications using Gmail SMTP and a Google App Password.

**Security:** Never upload Gmail passwords, App Passwords, or other secrets to GitHub.

## 🔍 Useful Docker Commands

Check running containers:

```bash
sudo docker ps
```

View container logs:

```bash
sudo docker compose logs
```

Restart services:

```bash
sudo docker compose restart
```

Stop all services:

```bash
sudo docker compose down
```

## 💡 Key Learning Outcomes

- Understanding Docker architecture and container management.
- Working with Docker Compose.
- Configuring Prometheus scraping targets.
- Monitoring Linux system metrics using Node Exporter.
- Creating Grafana monitoring dashboards.
- Configuring Prometheus alert rules.
- Understanding Alertmanager and email notification setup.

## 🚀 Future Enhancements

- Deploy the monitoring stack on AWS EC2.
- Add more advanced monitoring dashboards.
- Configure Slack or Telegram notifications.
- Implement centralized monitoring for multiple servers.
- Add CI/CD automation for configuration updates.

## 👨‍💻 Author

**Navaneeth**

GitHub: https://github.com/Nani-software

---

⭐ If you find this project useful, feel free to explore the repository and learn from it.
