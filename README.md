# 🚀 Docker-based Monitoring Project

A comprehensive DevOps project showcasing containerized monitoring with Node.js application, Prometheus, Grafana, and Node Exporter. This project demonstrates industry best practices in containerization, monitoring, and CI/CD pipelines.

## 📋 Project Overview

This project implements a full-stack monitoring solution with:
- **Node.js Backend Application** with chatbot services
- **Prometheus** for metrics collection
- **Grafana** for data visualization
- **Node Exporter** for system metrics
- **Docker Compose** for orchestration
- **Jenkins CI/CD** pipeline
- **Terraform** for infrastructure as code (optional)

## 🏗️ Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Node.js App   │    │   Prometheus    │    │     Grafana     │
│   (Port 3000)   │───▶│   (Port 9090)   │───▶│   (Port 3001)   │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │                       │
         │                       │                       │
         ▼                       ▼                       ▼
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Node Exporter │    │   Docker Volumes │   │   Docker Network │
│   (Port 9100)   │    │   (Data Storage) │   │   (Communication)│
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

## 🛠️ Tech Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **Chatbot Services** - AI-powered interactions

### Monitoring
- **Prometheus** - Metrics collection and storage
- **Grafana** - Data visualization and dashboards
- **Node Exporter** - System metrics exporter

### DevOps
- **Docker** - Containerization
- **Docker Compose** - Multi-container orchestration
- **Jenkins** - CI/CD pipeline
- **Terraform** - Infrastructure as code

### Security
- **SSL/TLS** - HTTPS encryption
- **Environment Variables** - Configuration management
- **Docker Security** - Container isolation

## 🚀 Quick Start

### Prerequisites
- Docker & Docker Compose
- Node.js 16+ (for local development)
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/monitoring-project.git
   cd monitoring-project
   ```

2. **Environment Setup**
   ```bash
   # Copy and configure environment variables
   cp App/.env.example App/.env
   # Edit .env with your configuration
   ```

3. **Start the Application**
   ```bash
   # Using Docker Compose (Recommended)
   docker-compose up -d
   
   # Or for local development
   cd App
   npm install
   npm start
   ```

4. **Access Services**
   - **Node.js App**: http://localhost:3000
   - **Prometheus**: http://localhost:9090
   - **Grafana**: http://localhost:3001
   - **Node Exporter**: http://localhost:9100

## 📊 Monitoring Setup

### Prometheus Configuration
- **Configuration File**: `monitoring/prometheus.yml`
- **Scrape Interval**: 15 seconds
- **Targets**: Node.js App, Node Exporter

### Grafana Dashboards
- **System Metrics**: CPU, Memory, Disk usage
- **Application Metrics**: Request rates, Response times
- **Custom Dashboards**: Business KPIs

## 🔧 Development

### Project Structure
```
├── App/                    # Node.js application
│   ├── utils/             # Service modules
│   ├── prompts/           # Chatbot prompts
│   ├── public/            # Static files
│   └── uploads/           # User uploads
├── monitoring/            # Monitoring configuration
│   ├── prometheus.yml     # Prometheus config
│   └── grafana/           # Grafana dashboards
├── terraform/            # Infrastructure code
├── Dockerfile            # Application container
├── docker-compose.yml    # Multi-container setup
└── Jenkinsfile          # CI/CD pipeline
```

### Local Development
```bash
# Install dependencies
cd App && npm install

# Start development server
npm run dev

# Run tests
npm test

# Build for production
npm run build
```

## 🔄 CI/CD Pipeline

### Jenkins Pipeline Stages
1. **Code Checkout** - Pull latest code
2. **Security Scan** - Vulnerability assessment
3. **Build** - Create Docker image
4. **Test** - Run automated tests
5. **Deploy** - Push to registry and deploy

### Pipeline Commands
```bash
# Trigger Jenkins build
curl -X POST http://jenkins-server/job/monitoring-project/build

# View pipeline status
http://jenkins-server/job/monitoring-project
```

## 🌐 Deployment

### Docker Deployment
```bash
# Production deployment
docker-compose -f docker-compose.prod.yml up -d

# Scale services
docker-compose up -d --scale app=3
```

### Terraform Deployment (Optional)
```bash
cd terraform
terraform init
terraform plan
terraform apply
```

## 📈 Monitoring & Alerting

### Key Metrics
- **Application**: Response time, Error rate, Throughput
- **System**: CPU usage, Memory usage, Disk I/O
- **Infrastructure**: Container health, Network latency

### Alerting Rules
- High CPU usage (>80%)
- Memory pressure (>90%)
- Application errors (>5%)
- Service downtime

## 🔒 Security Features

- **SSL/TLS Encryption** - HTTPS communication
- **Environment Variables** - Secure configuration
- **Docker Security** - Container isolation
- **Security Scanning** - Automated vulnerability checks
- **Access Control** - Role-based permissions

## 🧪 Testing

```bash
# Run unit tests
npm test

# Run integration tests
npm run test:integration

# Run security tests
npm run security:scan

# Run performance tests
npm run test:performance
```

## 📚 API Documentation

### Application Endpoints
- `GET /` - Health check
- `GET /metrics` - Application metrics
- `POST /chatbot` - Chatbot interaction
- `GET /api/status` - Service status

### Monitoring Endpoints
- `GET /metrics` - Prometheus metrics
- `GET /health` - Health check

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙋‍♂️ Support

- **Issues**: [GitHub Issues](https://github.com/yourusername/monitoring-project/issues)
- **Discussions**: [GitHub Discussions](https://github.com/yourusername/monitoring-project/discussions)
- **Email**: your.email@example.com

## 🏆 Acknowledgments

- [Prometheus](https://prometheus.io/) - Monitoring system
- [Grafana](https://grafana.com/) - Visualization platform
- [Docker](https://www.docker.com/) - Container platform
- [Node.js](https://nodejs.org/) - JavaScript runtime

---

**⭐ Star this repository if it helped you!**

**🔄 Fork and contribute to make it better!**