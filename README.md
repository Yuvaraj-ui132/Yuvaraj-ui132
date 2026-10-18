<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=200&section=header&text=Yuvaraj%20Murkunde&fontSize=46&fontColor=ffffff&fontAlignY=38&desc=Backend%20and%20AI%20Engineer&descAlignY=58&descSize=20" alt="Yuvaraj Murkunde, Backend and AI Engineer" width="100%">

**Final-year B.E. Information Science · KLS Gogte Institute of Technology, Belagavi · Class of 2027**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)

![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)

</div>

> [!NOTE]
> 🎯 **Open to work:** 2026–27 backend / SDE internships and fresher roles (India or remote)
> 📧 [yuvarajbmbm@gmail.com](mailto:yuvarajbmbm@gmail.com) · 💼 [LinkedIn](https://www.linkedin.com/in/yuvaraj-murkunde-46a828378)

<div align="center">

[**About**](#-about) · [**Projects**](#-featured-projects) · [**Skills**](#-skills) · [**Contact**](#-contact)

</div>

---

## 👋 About

Hi, I'm Yuvaraj. I'm a final-year Information Science student in Belagavi who likes the parts of software that happen behind the screen: queues, APIs, databases, and the tests that keep them honest.

I build backend systems in Python and FastAPI, from an async code-judging pipeline to a RAG-based AI travel assistant, and I ship them with tests, CI and Docker.

<div align="center">

| 174 | 239 | 102 | 31 | 150+ |
|:---:|:---:|:---:|:---:|:---:|
| problems in AlgoQuest | tests in AlgoQuest | tests in the Belagavi backend | destinations in the tourism app | DSA problems solved |

</div>

| What I focus on | |
|---|---|
| ⚙️ **Reliability** | async job queues, retries, lease heartbeats, crash recovery |
| 🔐 **Security** | server-side token verification, rate limiting, hidden test cases kept off the client |
| 🧪 **Testing** | pytest suites, PostgreSQL integration tests, GitHub Actions CI |
| 🤖 **Applied AI** | retrieval-augmented generation grounded in a verified database |

---

## 🚀 Featured projects

### 1. AlgoQuest: a DSA practice platform with its own code judge

[![Live Demo](https://img.shields.io/badge/Live_Demo-Open-2ea44f?style=for-the-badge&logo=googlechrome&logoColor=white)](https://algoquest-9aab0.web.app)
[![Source](https://img.shields.io/badge/Source_Code-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Yuvaraj-ui132/AlgoQuest)

**The problem:** interview practice is scattered across problem sheets, editors and tracking spreadsheets. AlgoQuest puts the problems, a code editor, a real judge and progress tracking in one place.

**What I built**
- **Practice workspace:** 174 curated problems across 14 topics (Arrays, Trees, Graphs, DP and more) with a Monaco editor (the VS Code engine) supporting C, C++17, Java 17, Python 3 and JavaScript
- **Two ways to run code:** a quick **Run** against sample tests, and a full **Submit** against hidden tests through an asynchronous pipeline (HTTP 202, then client polling)
- **Safe code execution:** code runs in sandboxes through Judge0 CE, with per-test verdicts, runtime and memory reporting
- **Reliable queueing:** an in-memory `asyncio` queue for simple deployments, plus a durable PostgreSQL queue mode using `FOR UPDATE SKIP LOCKED`, lease heartbeats and orphan recovery
- **Security:** hidden test cases stay on the server, Firebase ID tokens are verified server-side, per-user token-bucket rate limiting (10 submissions per minute), security headers, structured logging with request IDs
- **Progress tracking:** submission history, verdict and language breakdowns, a dashboard, bookmarks and revision tracking
- **Quality:** **239 tests** across 13 modules (including PostgreSQL integration tests), Ruff linting, GitHub Actions CI, a non-root Docker image and Docker Compose for local development

<details>
<summary><b>How a submission flows</b></summary>

1. The browser sends the code with the user's Firebase ID token
2. The backend verifies the token and checks the rate limit
3. The job is queued and the API answers immediately with `202` and a job ID
4. A worker picks it up (in-memory queue, or the PostgreSQL queue with leases and heartbeats)
5. Judge0 runs the code against the hidden test suite on the server
6. The client polls `GET /api/submissions/{job_id}` until a verdict arrives, and the result is stored in the user's history

</details>

`Python` `FastAPI` `PostgreSQL` `Firebase Auth` `Judge0 CE` `Docker` `GitHub Actions` `Vanilla JS`

---

### 2. Belagavi Smart Tourism: Android app and PWA with an AI travel guide

[![Live Web App](https://img.shields.io/badge/Live_Web_App-Open-2ea44f?style=for-the-badge&logo=googlechrome&logoColor=white)](https://belagavi-tourism-planner.web.app)
[![Android APK](https://img.shields.io/badge/Android_APK-v1.0.0-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://github.com/Yuvaraj-ui132/Belagavi_Tourism/releases/tag/v1.0.0)
[![Source](https://img.shields.io/badge/Source_Code-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Yuvaraj-ui132/Belagavi_Tourism)

**The problem:** regional travel information is scattered across blogs and outdated listings, and a generic chatbot can invent opening hours or fees. This app combines a curated database with an AI guide whose facts are checked against it.

**What I built**
- **Two clients, one backend:** a native Android app (Kotlin, Jetpack Compose, Material 3, MVVM, Hilt, Retrofit, Coroutines) and an installable PWA with offline caching, both using the same FastAPI backend
- **31 curated destinations** (forts, waterfalls, temples, wildlife) with an interactive map (Leaflet + OpenStreetMap), category filters, GPS distance and routing
- **Hybrid RAG assistant:** a query router sends local questions to pgvector semantic search (Gemini embeddings) and time-sensitive ones (weather, events) to Tavily live web research, run concurrently
- **Grounded answers:** facts like entry fees, coordinates and visit duration are re-inserted from verified PostgreSQL rows after the model writes its answer, and a fallback chain across Gemini models keeps the guide working if one fails
- **Travel tools:** wishlist, trip budget and expense tracker, and community ratings and reviews, synced between web and Android through Cloud Firestore
- **Security:** server-side Firebase ID-token verification on the chat endpoint, PostgreSQL row-lock rate limiting (20 requests per minute per user), and per-user Firestore security rules
- **Quality:** **102 backend tests**, a signed release APK (R8-minified, target SDK 34), and the API deployed serverless on Vercel

<details>
<summary><b>How the AI guide answers a question</b></summary>

1. The Firebase ID token is verified and the rate limit is checked
2. Greetings take a fast path and skip the model
3. The query router decides: local knowledge, or live web research as well
4. The question is embedded (Gemini, 768 dimensions) and matched against destinations with pgvector cosine search
5. If needed, Tavily web research runs with a 5-second timeout, then falls back to local context
6. Gemini writes the answer under strict grounding rules
7. Verified facts (fees, coordinates, durations) are re-inserted from the database
8. A structured JSON response goes back to the Android or web client

</details>

`Kotlin` `Jetpack Compose` `FastAPI` `PostgreSQL + pgvector` `Gemini` `Tavily` `Firebase` `Vercel`

---

### 3. SoilAI Cloud Lab: soil compaction analysis for geotechnical engineering

[![Live Demo](https://img.shields.io/badge/Live_Demo-Open-2ea44f?style=for-the-badge&logo=googlechrome&logoColor=white)](https://soilai-691b5.web.app/soil-test)
[![Source](https://img.shields.io/badge/Source_Code-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Yuvaraj-ui132/SoilAi)

**The problem:** soil compaction tests produce lab readings that engineers calculate and plot by hand. SoilAI brings that workflow online: enter the trial data and get the engineering results.

**What I built**
- **Compaction analysis:** calculates moisture content and dry density from laboratory trial data
- **Engineering results:** builds compaction curves with quadratic curve fitting and determines Optimum Moisture Content (OMC) and Maximum Dry Density (MDD)
- **Zero air voids:** plots the theoretical zero-air-voids curve alongside the compaction results
- **Reliable calculations:** input validation and numerical safeguards (Pydantic, NumPy) to improve reliability
- **Reports and data:** PDF report generation, interactive Chart.js visualizations, and Firebase for sign-in and cloud data

`Python` `Flask` `NumPy` `Pydantic` `Chart.js` `Firebase` `Docker`

---

## 🛠️ Skills

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
<summary><b>Other work (ML experiments)</b></summary>

- [Customer Segmentation Dashboard](https://github.com/Yuvaraj-ui132/SCT_ML_2): K-Means with PCA, Streamlit
- [Home Vision](https://github.com/Yuvaraj-ui132/SCT_ML_1): real estate price regression, Streamlit
- [Hand Gesture Recognition](https://github.com/Yuvaraj-ui132/Hand-Gesture-Recognition): OpenCV landmark detection

</details>

---

## 📬 Contact

<div align="center">

[![Email](https://img.shields.io/badge/Email-yuvarajbmbm@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:yuvarajbmbm@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/yuvaraj-murkunde-46a828378)
[![LeetCode](https://img.shields.io/badge/LeetCode-Profile-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/u/Yuvaraj1718/)

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=100&section=footer" width="100%" alt="">

</div>
