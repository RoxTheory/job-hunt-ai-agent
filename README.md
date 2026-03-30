🤖 AI Recruitment Assistant (n8n + Gemini)
📌 Overview
This project is a self-hosted automation agent designed to analyze job descriptions and generate tailored cover letters. It leverages AI to compare specific job requirements against my actual technical background and certifications, providing a data-driven approach to job applications.

🛠 Tech Stack
Orchestration: n8n (Self-hosted via Docker)

AI Model: Google Gemini 2.5 Flash

Infrastructure: Docker Desktop on Windows

Target Profile: Junior System & Cloud Administrator (AZ-104 Certified)

🏗️ Infrastructure & Deployment
The application is containerized for consistency and ease of deployment. It uses a persistent volume to ensure that all workflows and credentials remain intact across restarts.

Persistence: Local volume mapping ${HOME}/n8n_data to /home/node/.n8n.

Orchestration: Managed via docker-compose.

Deployment Command:

Bash
docker-compose up -d
<p align="center">
<img width="462" height="80" alt="dockercompose" src="https://github.com/user-attachments/assets/4f79e35f-e928-46e2-a076-14da3945f900" />
</p>

⚙️ How it Works
Input: A job description is pasted into the n8n Agent node.

Analysis: The agent extracts key requirements and matches them against my CV stored in a dedicated "Source of Truth" node.

Structured Output: The AI generates a match score, identifies skill gaps, and drafts a personalized cover letter.

Automated Mailing: A professional HTML report is sent directly to a dedicated Gmail folder.

🔑 Google Cloud Integration & Security
The system is securely linked to the Google Cloud Console to automate the delivery of analysis reports:

OAuth 2.0 Authentication: Configured a dedicated project with the Gmail API enabled.

Secure Credentials: Implemented Client ID and Client Secret handshake within n8n.

API Management: Integrated Google AI Studio keys to power the Gemini 2.5 Flash model.

🤖 Advanced Workflow Logic
The workflow implements sophisticated data processing to ensure professional results:

Structured Output Parsing: Enforced a rigid JSON Schema to guarantee data integrity:

JSON
{
  "nom_du_poste": "string",
  "score": "number",
  "commentaire": "string",
  "lettre_de_motivation": "string"
}
Dynamic HTML Templating: Built a custom HTML/CSS email template to render reports with a color-coded match badge.

Smart Routing & Aliasing: - Used Gmail Plus Addressing (+new) to target specific filters.

Automated Labeling: Configured Gmail filters to categorize reports into JobSearch/Newoffers.

<p align="center">
<img width="1213" height="559" alt="WorfklowJobHunt" src="https://github.com/user-attachments/assets/9b7ac121-03d1-4fb4-9c7b-247f7079065d" />
</p>

🚀 Key Learnings
Prompt Engineering: Implemented strict guidelines to prevent AI "hallucinations" regarding identity and certifications.

Docker Management: Mastered data persistence and container orchestration.

Low-Code Automation: Used n8n expressions to dynamically link nodes and automate the decision-making process.

📈 Future Roadmap
[ ] Data Logging: Connect a Google Sheets node to track application history.

[ ] Automated Triggering: Implement a URL scraper to analyze job postings directly from a link.

[ ] Skill Gap Analysis: Enhance prompts to generate learning paths for "Senior" roles.
