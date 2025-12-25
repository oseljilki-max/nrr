# Smart City IoT Infrastructure 2025

## 1. Жобаны басқару (Planning)
* **Әдістеме:** Lean Software Development
* **Құралдар:** GitHub Projects (Automation Suite)
* **Прогресс:** Прототиптеу кезеңі аяқталды

## 2. Технологиялық стек
* **Backend:** Go (Golang)
* **Хаттама:** MQTT & WebSockets
* **Деректер қоры:** InfluxDB (Time-series)
* **Бұлттық орта:** AWS IoT Core
* **Контейнерлеу:** Docker & Kubernetes

## 3. IoT Деректер ағынының схемасы
```mermaid
graph TD
    Sensors((Ақылды датчиктер)) --> Gateway[IoT Gateway]
    Gateway --> Broker[MQTT Broker: AWS IoT]
    Broker --> Processor[Data Processor: Go]
    Processor --> TSDB[(InfluxDB)]
    Processor --> Dashboard[Real-time Dashboard]
    
    subgraph "Edge Computing"
        Sensors
        Gateway
    end
    
    subgraph "Cloud Analysis"
        Broker
        Processor
        TSDB
    end
