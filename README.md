<h1 align="center">Rajan Patel</h1>
<h3 align="center">Backend-Focused Software Engineer · Distributed Systems & Scalable Platforms</h3>

<p align="center">
  <a href="https://rajanpatel.vercel.app/">Portfolio</a> ·
  <a href="https://www.linkedin.com/in/rajan-patel-5016a628a/">LinkedIn</a> ·
  <a href="mailto:rkp1505.l@gmail.com">Email</a> ·
  <a href="https://github.com/RajanPatel0">GitHub</a>
</p>

<p align="center">
  <img src="https://cdn.dribbble.com/users/1162077/screenshots/5403918/media/d5dccb5d7c2fbbf4f0fcf65340d8677f.gif" width="360" alt="Backend Development"/>
</p>

---

### About

Final-year B.Tech CSE student (IKGPTU, 2023–2027, CGPA 8.50) focused on backend and distributed systems. I've shipped production code across event-driven microservices (Kafka), dual-database consistency (Cassandra + PostgreSQL), payment webhook infrastructure, geospatial search, ML-backed forecasting, and LLM-orchestrated automation — not toy versions of these, the real failure-mode-handling versions.

I care most about the parts of a system most people skip: idempotency, race conditions, data consistency under concurrent writes, and what happens when the "happy path" breaks.

---

### Experience

**Backend Developer Intern — Small Fare™** · *Dec 2025 – Apr 2026*
- Engineered an event-driven Kafka pipeline (idempotent producer, exactly-once semantics, GZIP compression) decoupling booking, ticketing, and search-indexing services.
- Architected dual-database synchronization — Cassandra for high-throughput TTL-based ticket holds, PostgreSQL for ACID transactional records — reconciled via background drift-detection workers.
- Built a fault-tolerant webhook engine using Redis distributed locks (atomic Lua-script unlocks), 24h replay protection, and HMAC-verified payment confirmations.

**Full Stack Developer Intern — Wyreflow Technologies** · *Jul 2025 – Oct 2025*
- Developed a 3-tier RBAC system (Student / Sub-Admin / Super Admin) with custom JWT middleware and dynamic per-module, per-HTTP-method permission guards.
- Integrated Razorpay for memberships and paid bookings with HMAC-SHA256 signature verification and webhook-driven order lifecycle handling.
- Built the end-to-end job application workflow with real-time admin notifications (Node EventEmitter) and deadline-validated, state-tracked status transitions.

---

### Featured Projects

**[State University ERP — Alumni Network Platform](https://test.ptu.ac.in/alumni)** · *Next.js, TypeScript, PostgreSQL, Prisma, Redis*
A multi-tenant alumni portal live across 6 university campuses and 250+ affiliated colleges.
- Isolates data across 30+ relational models via indexed foreign keys, enforcing campus-scoped access.
- Built a foreign-key-based data normalization engine collapsing 40+ branch and 250+ company-name variants across 5,000+ records inside atomic Prisma transactions — took directory filter precision to 100%.
- Built a keyset-cursor-paginated notification worker (10K notifications in 2.39s) and a rate-throttled SMTP invite pipeline with zero bounces.

**[InVolv IN](https://involv.vercel.app)** · [`Source`](https://github.com/RajanPatel0/InVolv) · *MERN, Redis, FastAPI, OSRM*
A location-based product discovery platform connecting users to nearby local stores in real time.
- Geospatial discovery engine using MongoDB `$geoNear` + 2dsphere indexing, chained with Atlas fuzzy `$search` for typo-tolerant product matching.
- ML demand-forecasting microservice (FastAPI, statsmodels `SimpleExpSmoothing`) with Redis-cached (24h) responses for price-trend prediction.
- Real-time inventory analytics pipeline (Redis Hashes/Sets + hourly cron) powering automated restock and FCM price-drop alerts.

**Onwards AI — Voice-Guided Browser Navigation Agent** · [`Source`](https://github.com/RajanPatel0) · *React, Node.js, Groq/Gemini API, Web Speech API*
A voice-controlled AI agent that navigates any website hands-free from natural language commands.
- Orchestrates Web Speech API (ASR) with Groq Llama 3.3 / Gemini 2.0 LLM inference and deterministic DOM automation.
- Built a two-stage token-budgeting pipeline (DOM purification + 24K-char backend truncation) that cut LLM payload size by 70%.
- Eliminated selector hallucinations to 0% via a deterministic `data-unstuck-id` DOM-tagging and routing engine, replacing fragile LLM-generated CSS/XPath selectors.

---

### Tech Stack

**Languages**
<p>
  <img src="https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white"/>
  <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=c%2B%2B&logoColor=white"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white"/>
</p>

**Backend & Messaging**
<p>
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white"/>
  <img src="https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white"/>
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white"/>
  <img src="https://img.shields.io/badge/Apache_Kafka-000000?style=flat-square&logo=apachekafka&logoColor=white"/>
  <img src="https://img.shields.io/badge/REST_APIs-02569B?style=flat-square"/>
  <img src="https://img.shields.io/badge/Webhooks-6E56CF?style=flat-square"/>
</p>

**Databases & Caching**
<p>
  <img src="https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white"/>
  <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=flat-square&logo=mongodb&logoColor=white"/>
  <img src="https://img.shields.io/badge/Cassandra-1287B1?style=flat-square&logo=apachecassandra&logoColor=white"/>
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/>
  <img src="https://img.shields.io/badge/Prisma_ORM-2D3748?style=flat-square&logo=prisma&logoColor=white"/>
</p>

**Infra, Tools & AI/ML**
<p>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white"/>
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white"/>
  <img src="https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white"/>
  <img src="https://img.shields.io/badge/Scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white"/>
  <img src="https://img.shields.io/badge/LLM_Integration-Groq_%7C_Gemini-412991?style=flat-square"/>
</p>

---

### Achievements

- Solved 450+ Data Structures & Algorithms problems (LeetCode)
- University T&P Cell Coordinator and E-Cell Core Member — portal maintenance and startup initiatives
- Machine Learning training via IIT Madras Pravartak
- Finalist — HackMol 6.0 and PSB Hackathon 2025

---

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=RajanPatel0&show_icons=true&theme=radical&hide_border=true"/>
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=RajanPatel0&theme=radical&hide_border=true"/>
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=RajanPatel0&layout=compact&theme=radical&hide_border=true"/>
</p>

---

<p align="center">
  Open to backend / SDE internships and full-stack roles — reach out via <a href="mailto:rkp1505.l@gmail.com">email</a> or <a href="https://www.linkedin.com/in/rajan-patel-5016a628a/">LinkedIn</a>.
</p>
