# Stream Scan

[![License](https://img.shields.io/github/license/devops2626/stream-scan)](LICENSE)
[![Stars](https://img.shields.io/github/stars/devops2626/stream-scan)](https://github.com/devops2626/stream-scan/stargazers)
[![Issues](https://img.shields.io/github/issues/devops2626/stream-scan)](https://github.com/devops2626/stream-scan/issues)

[![CI](https://github.com/devops2626/stream-scan/actions/workflows/ci.yml/badge.svg)](https://github.com/devops2626/stream-scan/actions/workflows/ci.yml)
[![CD](https://github.com/devops2626/stream-scan/actions/workflows/cd.yml/badge.svg)](https://github.com/devops2626/stream-scan/actions/workflows/cd.yml)
[![CodeQL](https://github.com/devops2626/stream-scan/actions/workflows/codeql.yml/badge.svg)](https://github.com/devops2626/stream-scan/actions/workflows/codeql.yml)

**Real-time stream scanning and monitoring tool.**

> A high-performance tool for scanning, analyzing, and securing data, media, or network streams in real time.

---

## ✨ Features

- **Real-time Processing** — Scan streams with minimal latency
- **Multi-format Support** — Handles video, audio, log, network, and custom data streams
- **Threat Detection** — Malware scanning, anomaly detection, content filtering
- **Scalable Architecture** — Designed for high-throughput environments
- **Extensible** — Easy to add custom scanners and plugins
- **Monitoring & Alerts** — Built-in metrics, logging, and notification system
- **CLI + API** — Both command-line and REST/gRPC interfaces

## 🛠 Tech Stack

- **Language**: Python / Go (choose one)
- **Streaming**: FFmpeg, Kafka, RabbitMQ, or WebRTC
- **Scanning Engine**: [Your scanning library here]
- **Monitoring**: Prometheus + Grafana
- **Containerization**: Docker + Docker Compose

## 📦 Installation

### Prerequisites
- Docker (recommended)
- Python 3.11+ or Go 1.22+

### Using Docker (Recommended)

```bash
git clone https://github.com/devops2626/stream-scan.git
cd stream-scan
docker compose up -d
```

### From Source

```bash
git clone https://github.com/devops2626/stream-scan.git
cd stream-scan

# Python
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# Go
go mod tidy
```

## 🚀 Quick Start

```bash
# Scan a video stream
stream-scan --input rtsp://example.com/stream --mode video

# Scan log stream with custom rules
stream-scan --input kafka://topic --mode log --rules rules.yaml

# Run with API server
stream-scan api --port 8080
```

## Configuration

Copy `.env.example` to `.env` and adjust values:

```env
INPUT_SOURCE=rtsp://...
SCAN_MODE=video
THRESHOLD=0.85
ALERT_WEBHOOK=https://...
```

See [config/README.md](config/README.md) for detailed configuration options.

## 📁 Project Structure

```
stream-scan/
├── src/                 # Main source code
├── config/              # Configuration files
├── docker/              # Dockerfiles & compose
├── tests/               # Test suite
├── docs/                # Documentation
├── scripts/             # Utility scripts
└── .github/             # Workflows & templates
```

## 🤝 Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

**Made with ❤️ for the DevOps & Security community**