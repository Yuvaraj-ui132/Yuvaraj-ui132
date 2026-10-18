# Yuvaraj Murkunde

**Backend and AI Engineer** · Final-year B.E. Information Science, KLS Gogte Institute of Technology, Belagavi (2027)

I build backend systems in Python and FastAPI, from async job queues to RAG-based AI assistants, and I write tests for them.

**Open to** 2026–27 backend / SDE internships and fresher roles (India or remote)<br>
📧 [yuvarajbmbm@gmail.com](mailto:yuvarajbmbm@gmail.com) · 💼 [LinkedIn](https://www.linkedin.com/in/yuvaraj-murkunde-46a828378)

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=firebase&logoColor=black)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white)

---

## Featured projects

### [AlgoQuest](https://github.com/Yuvaraj-ui132/AlgoQuest): DSA practice platform with its own code judge
[Live demo](https://algoquest-9aab0.web.app) · [Source](https://github.com/Yuvaraj-ui132/AlgoQuest)

- **Practice workspace:** 174 problems across 14 topics, Monaco editor, code run in C, C++, Java, Python and JavaScript through Judge0 CE
- **Async submissions:** HTTP 202 + client polling, with an in-memory queue and a durable PostgreSQL queue mode (`SKIP LOCKED`, lease heartbeats, orphan recovery)
- **Fair judging:** hidden test cases stay server-side and are never sent to the browser
- **Security:** Firebase ID-token verification on the server, token-bucket rate limiting, security headers, structured logging with request IDs
- **Quality:** **239 tests** (including PostgreSQL integration tests), Ruff, GitHub Actions CI, non-root Docker image
- **Built with:** Python · FastAPI · PostgreSQL · Firebase · Judge0 · Docker

<a href="https://raw.githubusercontent.com/Yuvaraj-ui132/Yuvaraj-ui132/main/assets/algoquest-workspace.png"><img src="https://raw.githubusercontent.com/Yuvaraj-ui132/Yuvaraj-ui132/main/assets/algoquest-workspace.png" width="200" alt="AlgoQuest code workspace with an Accepted verdict"></a>
<a href="https://raw.githubusercontent.com/Yuvaraj-ui132/Yuvaraj-ui132/main/assets/algoquest-history.png"><img src="https://raw.githubusercontent.com/Yuvaraj-ui132/Yuvaraj-ui132/main/assets/algoquest-history.png" width="200" alt="AlgoQuest submission history"></a>
<a href="https://raw.githubusercontent.com/Yuvaraj-ui132/Yuvaraj-ui132/main/assets/algoquest-dashboard.png"><img src="https://raw.githubusercontent.com/Yuvaraj-ui132/Yuvaraj-ui132/main/assets/algoquest-dashboard.png" width="200" alt="AlgoQuest progress dashboard"></a>

<sub>Click a screenshot to enlarge.</sub>

### [Belagavi Smart Tourism](https://github.com/Yuvaraj-ui132/Belagavi_Tourism): Android app and PWA with an AI travel guide
[Live web app](https://belagavi-tourism-planner.web.app) · [Android APK](https://github.com/Yuvaraj-ui132/Belagavi_Tourism/releases/tag/v1.0.0) · [Source](https://github.com/Yuvaraj-ui132/Belagavi_Tourism)

- **Two clients, one backend:** native Android app (Kotlin, Jetpack Compose, MVVM, Hilt) and an offline-capable PWA with Leaflet maps, covering 31 curated destinations
- **Hybrid RAG assistant:** a query router sends local questions to pgvector semantic search (Gemini embeddings) and time-sensitive ones to Tavily live web research, run concurrently
- **Hallucination guard:** answers are checked against PostgreSQL records, with a fallback across Gemini models if one fails
- **Security:** Firebase ID-token verification on the chat endpoint, PostgreSQL-based rate limiting, per-user Firestore rules
- **Quality:** **102 backend tests**; chat history, wishlist, expenses and reviews synced between web and Android through Firestore
- **Built with:** Kotlin · Jetpack Compose · FastAPI · PostgreSQL + pgvector · Gemini · Firebase

<a href="https://raw.githubusercontent.com/Yuvaraj-ui132/Yuvaraj-ui132/main/assets/belagavi-ai-guide.png"><img src="https://raw.githubusercontent.com/Yuvaraj-ui132/Yuvaraj-ui132/main/assets/belagavi-ai-guide.png" width="200" alt="Belagavi AI Travel Guide on the web"></a>
<a href="https://raw.githubusercontent.com/Yuvaraj-ui132/Yuvaraj-ui132/main/assets/belagavi-map.png"><img src="https://raw.githubusercontent.com/Yuvaraj-ui132/Yuvaraj-ui132/main/assets/belagavi-map.png" width="200" alt="Belagavi interactive map of 31 destinations"></a>
<a href="https://raw.githubusercontent.com/Yuvaraj-ui132/Yuvaraj-ui132/main/assets/belagavi-android-chat.png"><img src="https://raw.githubusercontent.com/Yuvaraj-ui132/Yuvaraj-ui132/main/assets/belagavi-android-chat.png" width="110" alt="Belagavi AI Guide in the Android app"></a>

<sub>Click a screenshot to enlarge.</sub>

### [SoilAI Cloud Lab](https://github.com/Yuvaraj-ui132/SoilAi): soil compaction analysis for geotechnical engineering
[Live demo](https://soilai-691b5.web.app/soil-test) · [Source](https://github.com/Yuvaraj-ui132/SoilAi)

- **Compaction analysis:** calculates moisture content and dry density from laboratory trial data
- **Engineering curves:** generates compaction curves and finds Optimum Moisture Content (OMC) and Maximum Dry Density (MDD)
- **Zero air voids:** plots the theoretical zero-air-voids curve alongside the compaction results
- **Reliable calculations:** input validation and numerical safeguards (Pydantic, NumPy)
- **Reports and data:** PDF report generation, with data managed through Firebase
- **Built with:** Python · Flask · NumPy · Pydantic · JavaScript · Chart.js · Firebase · Docker

---

## Skills

| | |
|---|---|
| **Languages** | Python, Java, C++, C, JavaScript, Kotlin, SQL |
| **Backend** | FastAPI, Flask, REST APIs, asyncio, Pydantic |
| **Data** | PostgreSQL, pgvector, Cloud Firestore |
| **AI** | RAG, semantic search, Gemini API |
| **Mobile and Web** | Android (Jetpack Compose), PWA, JavaScript SPA, HTML/CSS |
| **Tools** | Git, GitHub Actions, Docker, Linux, pytest, Postman |
| **CS core** | DSA, OOP, DBMS, Operating Systems, Computer Networks |

<details>
<summary>Other work (ML experiments)</summary>

- [Customer Segmentation Dashboard](https://github.com/Yuvaraj-ui132/SCT_ML_2): K-Means with PCA, Streamlit
- [Home Vision](https://github.com/Yuvaraj-ui132/SCT_ML_1): real estate price regression, Streamlit
- [Hand Gesture Recognition](https://github.com/Yuvaraj-ui132/Hand-Gesture-Recognition): OpenCV landmark detection

</details>
