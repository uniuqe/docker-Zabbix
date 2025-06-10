# 🖥️ Docker-Zabbix Monitoring Stack

A complete monitoring stack using **Zabbix 7.2.9**, **PostgreSQL 16.2-alpine**, and **Grafana 12.0.0**, fully containerized with Docker Compose.

---

## 🚀 Quick Start

1. Clone the repository:

   git clone https://github.com/uniuqe/docker-Zabbix.git
   cd docker-zabbix
Create and edit the .env file with your configuration (example in .env.example).

Start the stack:
docker-compose up -d
Access the services:

Zabbix: http://localhost:8080
Default user: Admin
Default password: zabbix

Grafana: http://localhost:3000
Default user: admin
Default password: as set in .env or GF_SECURITY_ADMIN_PASSWORD

📦 Components
Zabbix Server with PostgreSQL backend
Zabbix Web Frontend (Nginx + PHP)
Zabbix Agent 2
PostgreSQL 16.2 (Alpine)
Grafana 12.0.0 with Zabbix datasource plugin

⚙️ Configuration
Edit .env file to configure:
POSTGRES_USER=zabbix
POSTGRES_PASSWORD=your-strong-password
POSTGRES_DB=zabbix
GF_SECURITY_ADMIN_USER=admin
GF_SECURITY_ADMIN_PASSWORD=your-strong-password
TZ=Asia/Tehran

🛠️ Useful Commands
View logs:
docker-compose logs -f zabbix-server
docker-compose logs -f postgres
docker-compose logs -f grafana

Stop and remove containers:
docker-compose down

Restart stack:
docker-compose restart

🔒 Security Notes
Change all default passwords before production use.
Use secure .env files and avoid committing sensitive data.
Consider enabling HTTPS on Grafana and Zabbix frontend for production.

📄 License
This project is open source and available under the MIT License.
