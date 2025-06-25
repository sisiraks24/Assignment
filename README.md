# Assignment
#  Docker Compose: Nginx Reverse Proxy with Go and Python Microservices

This project demonstrates a Docker Compose setup for running two microservices behind an Nginx reverse proxy. One microservice is written in Go, and the other in Python (Flask). Nginx handles path-based routing and logs incoming requests.

---

##  Services Overview

- **service_1**: A Go app exposing `/ping` and `/hello`
- **service_2**: A Python Flask app exposing `/ping` and `/hello`
- **nginx**: Acts as a reverse proxy, forwarding requests to the appropriate backend based on URL path

---

##  Setup Instructions

###  Clone the Repo

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
