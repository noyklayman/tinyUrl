# 🔗 TinyURL – Distributed URL Shortening Service

A scalable URL shortening platform built with **Java 11** and **Spring Boot**, designed to generate short links, manage URL redirections, and collect usage analytics using distributed data storage technologies.

The project demonstrates backend development concepts such as caching, distributed databases, REST APIs, and scalable system architecture.

---

## 📌 Project Overview

TinyURL allows users to convert long URLs into short and shareable links.

When a shortened URL is accessed, the system efficiently retrieves the original URL using a caching layer and records click activity for analytics purposes.

The application combines multiple storage technologies to optimize performance and scalability:

* **Redis** for fast caching and real-time counters
* **MongoDB** for URL persistence
* **Cassandra** for click history and event logging

---

## ⚙️ Technologies Used

| Technology  | Purpose                     |
| ----------- | --------------------------- |
| Java 11     | Core development            |
| Spring Boot | REST API framework          |
| MongoDB     | URL storage                 |
| Redis       | Caching layer               |
| Cassandra   | Analytics and click logging |
| Docker      | Containerized deployment    |
| Maven       | Dependency management       |

---

## ✨ Features

* Generate unique shortened URLs
* Redirect users to the original destination
* Store URL mappings in MongoDB
* Cache frequently accessed URLs using Redis
* Track user clicks and activity
* Store analytics data in Cassandra
* RESTful API architecture
* Docker-ready deployment

---

## 🔁 Application Workflow

### 1. Create a Short URL

Users submit a long URL through the API.

The application generates a unique short identifier and stores the URL mapping.

### 2. URL Storage

* URL data is stored in MongoDB.
* Frequently accessed URLs are cached in Redis.

### 3. Redirection

When a short URL is requested:

* Redis is checked first.
* If not found, MongoDB is queried.
* The user is redirected to the original URL.

### 4. Analytics Collection

Every URL access generates an event that is recorded for future analysis.

Analytics data includes:

* URL identifier
* Access timestamp
* Click count
* User activity information

### 5. Reporting

Stored analytics can be used to generate usage statistics and access reports.

---

## 🚀 Running the Project

```bash
mvn clean install
docker-compose up
```

The application will start all required services and expose the TinyURL API.

---

## 📚 Key Concepts Demonstrated

* REST API Development
* Spring Boot Architecture
* Distributed Databases
* Caching Strategies
* URL Redirection Logic
* Docker Containers
* Scalable Backend Design

Passionate about backend development, scalable systems, and modern software architecture.

