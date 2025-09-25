# 🌐 Netra — AI Cloud & Network Co-Pilot 🚀  
**Your AI-powered mobile-first app that makes cloud & network monitoring human-friendly with explanations, predictions, and fixes.**

---

![Made with Flutter](https://img.shields.io/badge/Made%20with-Flutter-blue?logo=flutter)
![Node.js Backend](https://img.shields.io/badge/Backend-Node.js-green?logo=node.js)
![OpenAI](https://img.shields.io/badge/Powered%20by-OpenAI-black?logo=openai)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Status](https://img.shields.io/badge/Status-MVP-orange)

---

## 📖 Overview  
Traditional monitoring dashboards (AWS CloudWatch, Datadog, Grafana) are **too technical** and **cluttered**. Small teams and students **don’t have DevOps experts** to interpret logs, metrics, and alerts.  

**Netra** solves this by providing:  
- 📡 Real-time telemetry monitoring  
- 🤖 **GenAI Copilot** that explains metrics in plain English  
- ⚡ Predictive alerts (outages, bandwidth spikes, risks)  
- 📱 A sleek **Flutter mobile app** + **Node.js backend**  

---

## ✨ Features (MVP)
- 🔴 **Live telemetry feed** (via WebSockets)  
- 🧾 **Event history** (in-memory for now, DB-ready)  
- 🤖 **AI Explain** button → human-readable summaries + 2 action steps  
- 🔔 **Alerts & notifications** (expandable to FCM)  
- ⚙️ **Cloud-ready** (Firebase, AWS, GCP integrations coming soon)

---
## 📚 Resources
- [Flutter Docs](https://flutter.dev)  
- [Node.js](https://nodejs.org)  
- [Docker](https://docs.docker.com)  
- [Firebase](https://firebase.google.com/docs)  
- [OpenAI API Docs](https://platform.openai.com/docs/quickstart)  

## 🛠 Tech Stack
- **Frontend (Mobile):** Flutter  
- **Backend:** Node.js + Express + WebSocket  
- **AI Layer:** OpenAI API (explanations, recommendations)  
- **Transport:** REST + WebSockets  
- **Infra:** Docker, Kubernetes/Cloud Run (future)  
- **Storage:** In-memory (MVP) → Firestore/Postgres (planned)  

---

## 📲 Screenshots (MVP Preview)
 

- 📡 **Dashboard:** See live events in a feed  
- 🤖 **Copilot Chat:** Ask “Why did latency spike?” and get an answer  
- 📊 **Graphs (Future):** Charts for latency, packet loss, and bandwidth  

---

## ⚡ Quickstart (Local Setup)

### 1️⃣ Clone repo
```bash
git clone https://github.com/<your-username>/Netra.git
cd Netra
2️⃣ Backend (Node.js)
cd backend
npm install
Create .env:

PORT=3000
OPENAI_API_KEY=sk-yourkeyhere
Run server:

node index.js
3️⃣ Mobile (Flutter)
cd mobile
flutter pub get
flutter run
👉 Use 10.0.2.2:3000 for Android emulator, localhost:3000 for iOS, or your machine’s IP for a real device.
4️⃣ Send test telemetry
curl -X POST http://localhost:3000/api/telemetry \
 -H "Content-Type: application/json" \
 -d '{"deviceId":"dev1","metricType":"latency_ms","value":120,"ts":"2025-09-25T12:00:00Z","meta":{"target":"api.example.com"}}'


You’ll see it appear in the Flutter app instantly. 🚀
📡 API Reference (MVP)
POST /api/telemetry

Submit telemetry event.

GET /api/events

Fetch recent events.

POST /api/explain

Ask GenAI to explain context.

GET /health

Health check.

WebSocket /ws

Pushes live telemetry events.
## 🚀 Deployment

Backend can run in **Docker**:

```bash
docker build -t netra-backend .
docker run -p 3000:3000 --env OPENAI_API_KEY=$OPENAI_API_KEY netra-backend

- Deploy on **Cloud Run**, **AWS ECS/Fargate**, or **Kubernetes**  
- Use **managed secrets** (AWS Secrets Manager, GitHub Secrets)  
- Always use **HTTPS/WSS** in production  

---

## 🔒 Security & Cost

- ❌ Never commit your `OPENAI_API_KEY`  
- ✅ Use `.gitignore` for `.env`  
- 💸 AI calls cost tokens → batch or summarize logs  
- ⚡ Add rate-limiting to `/api/explain`  

---

## 🛣️ Roadmap

- ✅ MVP (this repo)  
- 🔜 Cloud integrations (Firebase, AWS CloudWatch, GCP Monitoring)  
- 🔜 Graphs + dashboards in Flutter  
- 🔮 Predictive ML anomaly detection  
- 🔮 Team collaboration (Slack/Discord alerts)  





