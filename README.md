# 🤖 Assistant de Recrutement IA (n8n + Gemini)

## 📌 Présentation
Ce projet est un agent d'automatisation auto-hébergé conçu pour analyser des offres d'emploi et générer des lettres de motivation personnalisées. Il utilise l'IA pour comparer les exigences d'un poste avec mon profil technique réel.

## 🛠 Stack Technique
- **Orchestration :** n8n (Auto-hébergé via Docker)
- **Modèle d'IA :** Google Gemini 2.5 Flash
- **Infrastructure :** Docker Desktop sur Windows
- **Profil Cible :** Junior Administrateur Système & Cloud (Certifié AZ-104)

## ⚙️ Fonctionnement
1. **Entrée :** Je colle le texte d'une offre d'emploi dans l'agent n8n.
2. **Analyse :** L'agent extrait les compétences clés et les compare à mon CV stocké dans un nœud dédié.
3. **Sortie :** L'IA génère un score de match, liste les compétences manquantes (pour orienter ma veille) et rédige une lettre de motivation honnête.

## 🚀 Apprentissages Clés
- **Prompt Engineering :** Mise en place de consignes strictes pour éviter les "hallucinations" de l'IA (nom, diplômes, certifications).
- **Gestion Docker :** Déploiement et persistance des données avec des volumes locaux.
- **Automatisation Low-Code :** Manipulation des expressions n8n pour lier les nœuds entre eux.
