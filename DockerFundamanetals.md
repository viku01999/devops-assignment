# Docker Fundamentals Assignment (Explanation Only)

## Objective

Understand how to use **Docker Compose** to run a **multi-container application** step by step.

No code is included — only process explanation.

---

# What is Docker Compose?

Docker Compose is a tool that allows you to:

- Run multiple containers together
- Define all services in one configuration file
- Automatically connect containers in a network
- Start/stop everything with a single command

---

# Step-by-Step Process to Use Docker Compose

---

## Step 1: Install Docker

First, you need Docker installed on your system.

Check installation:

- Docker Engine
- Docker Compose plugin

Verify using:

- Docker version command
- Compose version command

If both are installed, you are ready.

---

## Step 2: Understand Multi-Container Application

A real application usually has multiple parts:

- Frontend (UI / web app)
- Backend (API / server logic)
- Database (data storage)

Instead of running them separately, Docker Compose runs them together.

---

## Step 3: Create Project Structure

You organize your project into folders like:

- frontend service folder
- backend service folder
- main configuration file for Docker Compose

Each service will later become a container.

---

## Step 4: Define Services Conceptually

You define what each container will do:

### Frontend service:
- Handles user interface
- Communicates with backend API

### Backend service:
- Handles business logic
- Sends/receives data

### Database service (optional):
- Stores persistent data

---

## Step 5: Create Docker Compose File (Concept)

Docker Compose file is where you define:

- All services (frontend, backend, database)
- How they are built
- Which ports they expose
- How they connect to each other

Think of it as a “blueprint” for your system.

---

## Step 6: Build Containers

Docker Compose will:

- Take each service definition
- Build Docker images (if needed)
- Create containers automatically

You do NOT manually create each container.

---

## Step 7: Internal Networking

One important feature:

Docker Compose automatically creates a network.

This allows:

- Frontend to talk to backend using service name
- Backend to connect to database
- No need for IP addresses

Example concept:

- frontend → backend service name
- backend → database service name

---

## Step 8: Start All Containers

With one command, Docker Compose:

- Starts frontend container
- Starts backend container
- Starts database container (if present)
- Connects them automatically

This is the main advantage of Docker Compose.

---

## Step 9: Access Application

After starting containers:

- Frontend runs on a browser port (example: 3000)
- Backend runs on API port (example: 5000)

You can test:

- Open frontend in browser
- It communicates with backend internally

---

## Step 10: Stop the Application

When finished:

- Docker Compose stops all containers together
- Removes network and temporary resources

This keeps system clean.

---

# Key Concepts Learned

## 1. Container Orchestration
Managing multiple containers together.

## 2. Service Definition
Each part of app is defined as a service.

## 3. Networking
Containers communicate using service names.

## 4. Automation
Single command manages entire system.

---

# Advantages of Docker Compose

- Easy multi-container setup
- Faster development workflow
- No manual container linking
- Consistent environments
- Simple startup and shutdown

---

# Real-World Use Case

Companies use Docker Compose for:

- Microservices architecture
- Full-stack applications
- Development environments
- Testing setups

---

# Conclusion

Docker Compose simplifies running complex applications by managing multiple containers as a single system. It helps developers avoid manual setup and ensures all services work together seamlessly.

---