# 🤖 AI Recruitment Assistant (n8n + Gemini)

## 📌 Overview
This project is a self-hosted automation agent designed to analyze job descriptions and generate tailored cover letters. It leverages AI to compare specific job requirements against my actual technical background and certifications.

## 🛠 Tech Stack
- **Orchestration:** n8n (Self-hosted via Docker)
- **AI Model:** Google Gemini 2.5 Flash
- **Infrastructure:** Docker Desktop on Windows
- **Target Profile:** Junior System & Cloud Administrator (AZ-104 Certified)

## ⚙️ How it Works
1. **Input:** Paste a job description into the n8n Agent node.
2. **Analysis:** The agent extracts key requirements and matches them against my CV stored in a dedicated "Source of Truth" node.
3. **Output:** The AI generates a match score, identifies skill gaps (to guide my technical watch), and drafts an honest, personalized cover letter.

## 🚀 Key Learnings
- **Prompt Engineering:** Implemented strict guidelines to prevent AI "hallucinations" regarding identity, degrees, and certifications.
- **Docker Management:** Deployed and managed data persistence using local volumes.
- **Low-Code Automation:** Used n8n expressions to dynamically link nodes and automate the decision-making process.
