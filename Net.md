# Client–Server Model (Networking Notes)

## What is Client–Server Model?
- It is a communication system where the **client** requests services and the **server** provides them.  
- Example: A web browser (client) requests a webpage from a web server.
- Client ---> Request ---> Server Client <--- Response <--- Server
- ---

## Components
- **Client:** Device or app that asks for data (browser, mobile app).  
- **Server:** Machine or software that provides data/service (web server, database server).  
- **Protocol:** Rules of communication (HTTP, TCP, UDP, FTP).  

---

## How Communication Works
1. Client sends a request to the server.  
2. Server listens on a port and receives the request.  
3. Server processes the request.  
4. Server sends back the response.  
5. Connection may close (stateless) or stay open (stateful).  

---

## Stateless vs Stateful
- **Stateless:** Each request is independent, no memory of previous ones. (Example: HTTP)  
- **Stateful:** Server remembers client session and state. (Example: TCP chat, online games)  

---

## Types of Architecture
- **2-Tier:** Client ↔ Server (direct communication).  
- **3-Tier:** Client ↔ Application Server ↔ Database.  
- **N-Tier / Microservices:** Many small services working together.  

---

## Advantages
- Centralized control of data and services.  
- Easy to manage and update.  
- Can be scaled vertically (bigger server) or horizontally (multiple servers).  

---

## Common Protocols
- **TCP:** Reliable and connection-based.  
- **UDP:** Faster but unreliable, used in gaming and streaming.  
- **HTTP/HTTPS:** For web communication.  
- **WebSocket:** For real-time two-way communication.  

---

## Example (Simple Idea)
- A browser opens `www.example.com`.  
- Browser (client) sends request → Web server receives request.  
- Server processes and sends webpage back to client.  

---

## Use Cases
- Websites and web apps.  
- Mobile apps connecting to backend servers.  
- Multiplayer online games.  
- Email servers, file servers, database servers.  

---

## Security Points
- Always use **HTTPS/TLS** for secure data transfer.  
- Use authentication (passwords, tokens, API keys).  
- Protect against attacks (firewall, rate limiting, input validation).  

---

## Conclusion
The Client–Server Model is the foundation of networking.  
It separates roles: **clients request, servers respond** — making systems organized, scalable, and secure.
