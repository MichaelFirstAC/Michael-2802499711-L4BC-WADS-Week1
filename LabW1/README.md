# Project 1: Github as a portfolio

* **Name:** Michael
* **Student ID:** 2802499711
* **Class:** L4BC

---

# Article: Securing Modern Microservices with Node.js and Git

## 1. The Shift from Monolith to Microservices
In traditional web development, applications were built as "monoliths"—single, large codebases where the user interface, database logic, and server-side code lived together. While simple to start, these become nightmares to maintain. 

Modern development has shifted toward **Microservices**. In this architecture, an application is broken down into small, independent services (e.g., a "User Service," a "Payment Service," and an "Inventory Service") that communicate over a network, typically using REST APIs or GraphQL.

> **Why it matters:** If the "Payment Service" crashes, the rest of the app (like browsing products) can still function. This is crucial for high-availability systems.

## 2. Security Challenges in Distributed Systems
While microservices offer scalability, they introduce complex security risks. Since services communicate over a network, the "attack surface" increases significantly.

### Key Vulnerabilities:
* **Insecure Communication:** Data moving between services can be intercepted if not encrypted.
* **Broken Authentication:** Managing user identity across multiple distinct services is difficult.
* **Dependency Risks:** Using many third-party libraries (like NPM packages in Node.js) increases the risk of supply chain attacks.

## 3. Best Practices for Securing Web Apps
To mitigate these risks, developers must implement robust security layers.

### A. Authentication & Authorization (JWT)
JSON Web Tokens (JWT) are the standard for stateless authentication. When a user logs in, they receive a signed token. They must present this token with every subsequent request. This allows services to verify identity without constantly checking a central database.

### B. HTTPS and TLS
All traffic, both external (user to server) and internal (service to service), must be encrypted using Transport Layer Security (TLS). This prevents "Man-in-the-Middle" attacks.

### C. Input Validation
Never trust user input. Whether using **FastAPI** (Python) or **Express** (Node.js), developers must validate incoming data to prevent Injection attacks (like SQL Injection or NoSQL Injection).

## 4. The Role of Git in DevSecOps
Security isn't just about code; it's about the workflow. Using **Git** allows teams to implement "DevSecOps"—integrating security checks directly into the version control process. By using branches (like `feature`, `testing`, and `main`), teams can review code for vulnerabilities before it ever reaches production.

---

### Visual References

**Figure 1: The Runtime Environment**
Node.js is frequently used to build lightweight, fast microservices due to its non-blocking I/O model.
![Node JS Logo](https://upload.wikimedia.org/wikipedia/commons/d/d9/Node.js_logo.svg)

**Figure 2: Version Control**
Git acts as the backbone of modern CI/CD pipelines, ensuring that every line of code is tracked and reviewable.
![Git Logo](https://git-scm.com/images/logos/downloads/Git-Logo-2Color.svg)