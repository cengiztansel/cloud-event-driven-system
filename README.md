# Cloud-Native Inventory Management System   [Turkish version below/ Türkçe versiyonu aşağıdadır]
This project is a Full-Stack application demonstrating how a modern, event-driven microservices architecture is deployed, scaled, and managed in a cloud environment (Google Cloud Platform).

# Live Demo: http://34.141.89.27:5173/
(Note: This is a showcase prototype with the security layer bypassed for demonstration purposes.)

# Tech Stack & Architecture
The project consists of a containerized ecosystem where each component has a specific responsibility:
•	Frontend: React + Vite (Fast and responsive UI)
•	Backend: Java 17 + Spring Boot 3.x
•	Database: PostgreSQL (Relational data management)
•	Event-Bus: Apache Kafka (Asynchronous inter-service communication)
•	Infrastructure: Docker & Docker Compose
•	Cloud: Google Cloud Platform (GCP) Compute Engine

# Key Features
•	Docker Containerization: The entire system is configured to be spun up with a single docker-compose up command.
•	Cloud Deployment: Deployed on GCP with custom firewall rules and network configurations.
•	Event-Driven Communication: Integrated with Apache Kafka to handle real-time data flow and decoupling.
•	RESTful API: Clean and extensible API endpoints following industry standards.

# System Workflow
1.	The user interacts with the React frontend to add or manage inventory.
2.	The Spring Boot backend processes the request and persists data in PostgreSQL.
3.	Simultaneously, the backend produces an event to a Kafka topic.
4.	Other services (or consumers) can subscribe to these events for real-time processing (e.g., logging, notification, or analytics).

# Local Installation
To run this project on your local machine:
1.	Clone the repository:
Bash
git clone https://github.com/cengiztansel/cloud-event-driven-system.git
2.	Navigate to the project directory:
Bash
    cd cloud-event-driven-system
    ```
3.  Start with Docker Compose:
    ```bash
    docker-compose up -d
    ```
4.  Access the services:
    *   **Frontend:** `http://localhost:5173`
    *   **Backend API:** `http://localhost:8080`

## About Me
I am **CengizTansel**, an Informatics Systems Specialist focused on bridging the gap between complex physical systems and the digital world. I am deeply passionate about Full-stack development and DevOps processes.

_____________________________________________________________________________________________________________________________________________________________

Turkish version/Türkçe versiyonu

# Cloud-Native Inventory Management System
Bu proje, modern bir mikroservis mimarisinin (Event-Driven) bulut ortamında (Google Cloud Platform) nasıl ölçeklenebilir ve yönetilebilir olduğunu kanıtlayan bir Full-Stack çalışmadır.

# Canlı Demo: http://34.141.89.27:5173/

# Teknolojiler ve Mimari
Proje, her bileşenin kendi sorumluluğuna sahip olduğu, Dockerize edilmiş bir ekosistemden oluşur:
•	Frontend: React + Vite (Hızlı ve responsive UI)
•	Backend: Java 21 + Spring Boot 3.x
•	Veritabanı: PostgreSQL (İlişkisel veri yönetimi)
•	Event-Bus: Apache Kafka (Servisler arası asenkron iletişim)
•	Infrastructure: Docker & Docker Compose
•	Cloud: Google Cloud Platform (GCP) Compute Engine
3 Mimari Şema
Sistem, kullanıcıdan gelen veriyi önce veritabanına kaydeder, ardından Kafka üzerinden bir event fırlatarak sistemin geri kalanını haberdar eder.

# Öne Çıkan Özellikler
•	Docker Containerization: Tüm sistem tek bir docker-compose up komutuyla ayağa kalkacak şekilde konfigüre edilmiştir.
•	Cloud Deployment: GCP üzerinde Firewall kuralları ve ağ yapılandırmalarıyla canlıya alınmıştır.
•	Event-Driven: Kafka entegrasyonu ile gerçek zamanlı veri akışı sağlanmıştır.
•	**(Prototip Modu - Güvenlik Katmanı “Keycloak” Devre Dışıdır. Sonraki sürümde yapılandırılacaktır)** 
•	RESTful API: Standartlara uygun, genişletilebilir API uçları.

# Yerel Kurulum (Local Setup)
Projeyi kendi bilgisayarınızda çalıştırmak için:
1.	Projeyi klonlayın:
Bash
git clone https://github.com/cengiztansel/cloud-event-driven-system.git
2.	Proje dizinine gidin:
Bash
cd cloud-event-driven-system
3.	Docker Compose ile başlatın:
Bash
    docker-compose up -d
    ```
4.  Erişim:
    *   **Frontend:** `http://localhost:5173`
    *   **Backend API:** `http://localhost:8080`

## Hakkımda
Ben **CengizTansel**, bir Bilişim Sistemleri Uzmanı olarak karmaşık sistemleri dijital dünyaya taşımaya, Full-stack geliştirmeye ve DevOps süreçlerinde 
derinleşmeye odaklanıyorum.
