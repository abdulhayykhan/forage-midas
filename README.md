# JPMC Midas Core - Advanced Software Engineering Simulation

A robust, enterprise-grade backend transaction processing system developed during the JPMorgan Chase & Co. Advanced Software Engineering Virtual Experience. This project simulates "Midas Core," a financial platform designed to handle high-frequency transactions with high availability and data integrity.

## 🚀 Key Features & Architecture

This project demonstrates a modern microservices-oriented architecture using a variety of industry-standard tools:

* **Message Queue Integration (Apache Kafka):** Implemented a Kafka listener to decouple the frontend from the backend, allowing for asynchronous communication and improved system scalability.
* **Data Persistence (Spring Data JPA & H2):** Integrated an H2 SQL database to record every transaction. Used JPA for object-relational mapping to ensure financial data resiliency and easy portability to production databases.
* **RESTful API Integration:** * **Incentive API:** Configured `RestTemplate` to communicate with an external microservice that calculates transaction incentives.
    * **Balance Query API:** Exposed a custom REST controller on port `33400` that allows users to query their account balances in real-time.
* **Validation Logic:** Implemented server-side validation to ensure sender/recipient validity and sufficient funds before processing any financial movement.

## 🛠️ Tech Stack

* **Language:** Java 17
* **Framework:** Spring Boot
* **Messaging:** Apache Kafka
* **Database:** H2 (In-memory SQL)
* **Tools:** Maven, Git, VS Code

## 📋 How to Run

1.  **Start Zookeeper & Kafka:** Ensure your local Kafka environment is running.
2.  **Start the Incentive Service:**
   ```powershell
    cd services
    java -jar transaction-incentive-api.jar
    ```
4.  **Run Midas Core:** Use your IDE or run the Maven wrapper:
    ```powershell
    ./mvnw spring-boot:run
    ```

## 🧪 Testing

The project includes comprehensive test suites for each module. To run the full integration tests:
```powershell
./mvnw test
```

---

*Developed by Abdul Hayy Khan as part of the JPMC Virtual Internship.*
