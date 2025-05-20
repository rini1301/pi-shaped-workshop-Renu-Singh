# pi-shaped-workshop-Renu-Singh

## 📁 Day 1 - Docker & Node.js Hello World App

- ✅ Created a simple Node.js REST API (`Hello, world!!`)
- ✅ Wrote a `Dockerfile` to containerize the app
- ✅ Built the Docker image with the tag `renu1301/hello-node-api:day1`
- ✅ Ran the container locally and exposed it on port `8080`
- ✅ Pushed the image to Docker Hub: [Docker Hub Image Link](https://hub.docker.com/repository/docker/renu1301/hello-node-api)

---


---

### 1. Why Docker is Useful in Building and Deploying Microservices

Docker helps developers package applications with everything they need—like libraries and settings—into small, isolated containers. This is useful for microservices for several reasons:

- **Same Environment Everywhere:** The app runs the same way on your computer, testing server, or production. No more "it works on my machine" problems.
- **Independent Services:** Each service runs in its own container, so they don’t interfere with each other even if they use different libraries or versions.
- **Faster Development and Delivery:** You can quickly build and launch containers, making it easier to release updates or new features regularly.
- **Efficient Resource Usage:** Containers are lightweight because they share the host OS, so they use less memory and start faster than traditional virtual machines.

---

### 2. Docker Image vs. Docker Container in the Context of Scaling

- **Docker Image:** It’s like a recipe or blueprint—it contains your app, its code, and everything it needs to run. It doesn't do anything by itself.
- **Docker Container:** It’s the running version of the image—a live app with all its files and dependencies.

When scaling:

- You **create more containers** from the same image to handle more traffic.
- This is called **horizontal scaling**—running more containers to share the load.

---

### 3. How Kubernetes Complements Docker for Scalability

Docker helps you run containers, but managing many containers across servers is hard. That’s where Kubernetes comes in:

- **Automatic Scaling:** It can add or remove containers based on system load or usage.
- **Traffic Distribution:** It spreads incoming traffic across all containers so nothing crashes under pressure.
- **No Downtime:** If something fails, Kubernetes restarts it or moves it to another healthy machine.
- **Safe Updates:** It lets you update your app without shutting it down and roll back if something goes wrong.
- **Service Communication:** Kubernetes helps containers find and talk to each other smoothly.

---

