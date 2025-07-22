# DevOps Microservices Project – User Registration System

 A hands-on microservices-based project demonstrating a simple yet powerful **DevOps workflow** using:

1 Python + Flask (Web API)
2 PostgreSQL (User registration storage)
3 Redis (Cache for fast data access)
4 Docker & Docker Compose (Service orchestration)

---

# Project Overview

This project contains **two separate microservices**:

###  Microservice 1: User Registration API
- Built with **Flask**
- Allows users to register via REST API
- Stores registration info in **PostgreSQL**

###  Microservice 2: Quick Access API
- Built with **Flask**
- Retrieves user data from **Redis cache** for faster response
- Pulls from PostgreSQL if cache misses



---

## ⚙ Tech Stack

  Component     | Tech Used               

 Language       | Python 3.x               
 Web Framework  | Flask                    
 Database       | PostgreSQL               
 Caching        | Redis                    
 DevOps Tools   | Docker, Docker Compose   

---

##  How It Works

### Step 1: User Registration
- User registers via `/register` endpoint
- Data is validated and stored in PostgreSQL

### Step 2: Quick Info Access
- When accessing `/user/name` in the Redis service:
  - It first checks Redis cache
  - If not found, it fetches from PostgreSQL and updates cache

---

##  API Endpoints

###  Registration Service

| Method | Endpoint     | Description              |
|--------|--------------|--------------------------|
| POST   | `/register`  | Register a new user      |

Example Request:
```json
{
  "name": "John Doe",
  "info": "john@example.com"
}



