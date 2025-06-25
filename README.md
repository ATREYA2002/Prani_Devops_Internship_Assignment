# 🧩 Multi-Service App with NGINX Reverse Proxy (Dockerized)

This project demonstrates a simple microservice architecture using:

- 🟦 **Golang Backend (Service 1)**
- 🐍 **Python/Flask Backend (Service 2)**
- 🌐 **NGINX as a Reverse Proxy**

All services are containerized with Docker and managed via Docker Compose. Everything is accessible on a **single port: `http://localhost:8081`** using path-based routing.

---

## 📁 Project Structure

├── docker-compose.yml
├── nginx
│ ├── nginx.conf
│ └── Dockerfile
├── service_1 # Golang service
│ └── Dockerfile
├── service_2 # Python service
│ └── Dockerfile
└── README.md

---
## ⚙️ How It Works

1. **Service 1** is a Golang API running on port `8001`
2. **Service 2** is a Python Flask API running on port `8002`
3. **NGINX** runs on port `80` internally, exposed to host as `8081`
4. NGINX uses path-based routing:
   - `/service1` → forwards to service 1
   - `/service2` → forwards to service 2

---

## 🚀 How to Set Up & Run

### 1️⃣ Prerequisites

- Docker installed: [Get Docker](https://www.docker.com/)
- Docker Compose installed

### 2️⃣ Clone the Repo

```
git clone https://github.com/ATREYA2002/Prani_Devops_Internship_Assignment.git
cd Prani_Devops_Internship_Assignment
```

🌐 Access the Services
Once running, open your browser or use curl:
```
Endpoint	Description
http://localhost:8081/service1/ping	Health check (Go)
http://localhost:8081/service1/hello	Hello from Go
http://localhost:8081/service2/ping	Health check (Python)
http://localhost:8081/service2/hello	Hello from Python
```



📝 What I Did
1)Created Dockerfiles for:

Golang service exposing port 8001
Python Flask service exposing port 8002
NGINX with custom routing config

2)Wrote nginx.conf to:

Reverse proxy to both services
Log request time, path, and client IP

3)Used Docker Compose to orchestrate the system with a single command


📊 Logs & Monitoring
To view NGINX access logs:
```
docker logs nginx
```






new
Here’s your updated and polished `README.md` with proper formatting and markdown consistency, ready for GitHub. I've fixed indentation, added headings, and wrapped everything in appropriate code blocks and tables.

---

```markdown
# 🧩 Multi-Service App with NGINX Reverse Proxy (Dockerized)

This project demonstrates a simple microservice architecture using:

- 🟦 **Golang Backend (Service 1)**
- 🐍 **Python/Flask Backend (Service 2)**
- 🌐 **NGINX as a Reverse Proxy**

All services are containerized with Docker and managed via Docker Compose. Everything is accessible on a **single port: `http://localhost:8081`** using path-based routing.

---

## 📁 Project Structure

```

.
├── docker-compose.yml
├── nginx
│   ├── nginx.conf
│   └── Dockerfile
├── service\_1         # Golang service
│   └── Dockerfile
├── service\_2         # Python service
│   └── Dockerfile
└── README.md

````

---

## ⚙️ How It Works

1. **Service 1** is a Golang API running on port `8001`
2. **Service 2** is a Python Flask API running on port `8002`
3. **NGINX** runs on port `80` internally, exposed to host as `8081`
4. NGINX uses path-based routing:
   - `/service1` → forwards to service 1
   - `/service2` → forwards to service 2

---

## 🚀 How to Set Up & Run

### 1️⃣ Prerequisites

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

---

### 2️⃣ Clone the Repo

```bash
git clone https://github.com/ATREYA2002/Prani_Devops_Internship_Assignment.git
cd Prani_Devops_Internship_Assignment
````

---

### 3️⃣ Start the System

```bash
docker-compose up --build
```

> This builds and starts all services.

---

## 🌐 Access the Services

Once running, open your browser or use `curl`:

| Endpoint                               | Description           |
| -------------------------------------- | --------------------- |
| `http://localhost:8081/service1/ping`  | Health check (Go)     |
| `http://localhost:8081/service1/hello` | Hello from Go         |
| `http://localhost:8081/service2/ping`  | Health check (Python) |
| `http://localhost:8081/service2/hello` | Hello from Python     |

---

## 📝 What I Did

1. **Created Dockerfiles** for:

   * Golang service exposing port `8001`
   * Python Flask service exposing port `8002`
   * NGINX with custom routing config

2. **Configured `nginx.conf`** to:

   * Reverse proxy to both services
   * Log request time, path, and client IP

3. **Used Docker Compose** to:

   * Build and run the full system using a single command

---

## 📊 Logs & Monitoring

To view NGINX access logs:

```bash
docker logs nginx
```

This logs requests with IP, timestamp, and request path for observability.

---

## ✅ Summary

* 🧱 Modular service-based setup
* 🌐 Single-port reverse proxy routing
* 🔁 Logs and health checks included
* 🐳 Fully containerized and orchestrated via Docker Compose

---

```

You can now paste this into your GitHub repo's `README.md`. It’s formatted cleanly and is ready for public sharing or submission. Let me know if you’d like badge icons (Docker, Go, Python, etc.) or a GIF demo!
```

