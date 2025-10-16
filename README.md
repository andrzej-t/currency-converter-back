# Currency Converter - Backend API

![Java](https://img.shields.io/badge/Java-17-orange?style=flat&logo=java)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.3.4-brightgreen?style=flat&logo=spring)
![Gradle](https://img.shields.io/badge/Gradle-8.x-blue?style=flat&logo=gradle)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat)

A high-performance RESTful API service for real-time currency conversion, integrating with the Polish National Bank (NBP) exchange rates. Built with modern Spring Boot and designed for reliability and scalability.

## ✨ Features

*   **Real-time Currency Conversion:** Convert between PLN and foreign currencies, or between two foreign currencies, using live exchange rates from the NBP API.
*   **Intelligent Caching:** Automatic caching of exchange rates (configurable TTL) to reduce external API calls and improve response times.
*   **Precision Handling:** Utilizes `BigDecimal` for accurate financial calculations with up to 2 decimal places.
*   **Robust Error Handling & Validation:** Global exception handling with meaningful error messages and comprehensive input validation.
*   **Full Test Coverage:** Includes unit, integration, and controller tests ensuring reliability and maintainability.

## 🛠 Technology Stack

*   **Backend:** Java 17, Spring Boot 3.3.4 (Spring Web, Spring Cache)
*   **Build:** Gradle 8.x, Lombok 1.18.26
*   **External API:** Polish National Bank (NBP) API
*   **Testing:** JUnit 5, Mockito, Spring Boot Test, MockMvc

## 🚀 Getting Started

1.  **Clone the repository:**
    ```bash
    git https://github.com/andrzej-t/currency-converter-back.git
    cd currency-converter-back
    ```
2.  **Build and run:**
    ```bash
    ./gradlew bootRun
    ```
    The application will be available at `http://localhost:8080`.

## 🔌 API Endpoints

**Base URL:** `http://localhost:8080/v1`

*   **Get All Available Currencies:**
    ```http
    GET /v1/currencies
    ```
*   **Convert Currency:**
    ```http
    GET /v1/result?amount={amount}&currencyFrom={from}&currencyTo={to}
    ```
    Example: `GET /v1/result?amount=100.50&currencyFrom=PLN&currencyTo=USD`

## 👤 Author & Links

*   **Author:** Andrzej Tyrpa (GitHub: @andrzej-t)
*   **Live Demo:** 
*   **Frontend Repository:** 

## 📄 License

This project is licensed under the MIT License.