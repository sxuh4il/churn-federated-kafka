# Churn Prediction with Federated Learning and Kafka

## Overview

This project implements a customer churn prediction system using Federated Learning and Apache Kafka for distributed data streaming.

## Features

- **Federated Learning**: Train machine learning models across multiple decentralized data sources without sharing raw data
- **Apache Kafka Integration**: Real-time data streaming and event processing
- **Churn Prediction**: Predict customer churn using distributed ML techniques
- **Privacy-Preserving**: Keep sensitive customer data local while collaborating on model training

## Project Structure

```
churn-federated-kafka/
├── src/
├── config/
├── data/
├── models/
├── kafka/
└── README.md
```

## Prerequisites

- Python 3.8+
- Apache Kafka
- Docker (optional)

## Installation

```bash
# Clone the repository
git clone https://github.com/username/churn-federated-kafka.git
cd churn-federated-kafka

# Install dependencies
pip install -r requirements.txt
```

## Configuration

1. Configure Kafka broker settings in `config/kafka.yml`
2. Set up federated learning parameters in `config/federated.yml`

## Usage

```bash
# Start Kafka services
docker-compose up -d

# Run the federated learning server
python src/server.py

# Run client nodes
python src/client.py --node-id 1
```

## Architecture

1. **Kafka Producer**: Streams customer data to topics
2. **Federated Server**: Coordinates model aggregation
3. **Federated Clients**: Train local models on private data
4. **Kafka Consumer**: Processes predictions and results

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

MIT License