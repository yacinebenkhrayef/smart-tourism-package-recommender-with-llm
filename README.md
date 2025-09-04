# smart-tourism-package-recommender-with-llm

## 1. Contexte du projet
Le secteur du tourisme en Tunisie et en Europe connaît une digitalisation croissante. Les plateformes de réservation et d’agences de voyage cherchent à améliorer l’expérience utilisateur en proposant des recommandations personnalisées et intelligentes. Ce projet vise à développer un système de recommandation de packages touristiques qui intègre un Large Language Model (LLM) pour permettre des requêtes en langage naturel et enrichir les recommandations.
________________________________________
## 2. Objectifs
•	Développer un moteur de recommandation hybride (filtrage collaboratif et filtrage par contenu) pour offrir des recommandations personnalisées et précises.
•	Permettre aux utilisateurs de formuler des requêtes en langage naturel (ex. : « Je cherche un séjour de 3 jours en montagne pour moins de 200€ »).
•	Améliorer l’expérience utilisateur en générant des descriptions de packages automatiquement adaptées au profil de l'utilisateur.
•	Fournir une démonstration interactive via une API et une interface utilisateur.
________________________________________
## 3. Périmètre fonctionnel
Fonctionnalités principales :
•	Recommandation personnalisée
o	Basée sur l’historique des réservations (filtrage collaboratif).
o	Basée sur les métadonnées des packages (filtrage par contenu).
o	Système hybride combinant les deux approches.
•	Recherche en langage naturel (LLM)
o	Compréhension des requêtes utilisateur pour en extraire les intentions et les entités clés (budget, destination, durée, activités).
o	Conversion des requêtes en filtres structurés pour le moteur de recherche.
•	Recherche sémantique
o	Utilisation d’embeddings (représentations vectorielles) pour trouver des packages similaires et gérer le problème de cold start.
•	Génération de descriptions intelligentes
o	Résumés marketing automatiques des packages, générés par le LLM et adaptés au profil de l'utilisateur.
•	Interface utilisateur & API
o	API REST (avec FastAPI) pour accéder aux recommandations.
o	Interface web simple (Streamlit) pour tester le système de bout en bout.
________________________________________
## 4. Architecture technique & Technologies
Architecture :
L'architecture sera modulaire, composée des éléments suivants :
•	Frontend : Interface web développée avec Streamlit.
•	Backend : Une API REST avec FastAPI qui servira de point d'entrée unique.
•	Moteur de Recommandation : Composant central utilisant scikit-learn pour le filtrage par contenu, et surprise ou LightFM pour le filtrage collaboratif.
•	Module LLM/NLP : Ce module gérera la compréhension du langage naturel (LangChain ou OpenAI) et la recherche sémantique (sentence-transformers, FAISS).
•	Base de Données : Une base de données relationnelle (ex: PostgreSQL ou SQLite pour la démo) pour stocker les données des packages, des utilisateurs et de leurs interactions.
Technologies :
•	Data & ML : Python 3.10+, pandas, scikit-learn, surprise, lightfm.
•	NLP/LLM : sentence-transformers, faiss, langchain, openai (ou des modèles open-source comme Mistral AI).
•	Backend : fastapi.
•	Frontend/Demo : streamlit.
•	Environnement : Git et GitHub pour le versioning et la collaboration.
________________________________________
## 5. Contraintes & Données
•	Données : Utilisation de datasets publics (Kaggle, Booking.com scrapes, Etnafes-like datasets) ou d'un jeu de données simulé de haute qualité.
•	Temps : 4 mois (septembre → décembre).
•	Qualité des données : Un effort de nettoyage et de standardisation sera réalisé pour garantir la pertinence des modèles.
________________________________________
## 6. Organisation & Planning (Macro)
•	Septembre (Phase 1) : Collecte des données, nettoyage, et développement d'un moteur de recommandation de baseline.
•	Octobre (Phase 2) : Développement du système hybride et de l'API REST avec FastAPI.
•	Novembre (Phase 3) : Intégration du LLM pour les requêtes naturelles et la recherche sémantique.
•	Décembre (Phase 4) : Finalisation du système, documentation, et préparation de la démonstration.
________________________________________
## 7. Critères de succès & Risques
Critères de Succès :
•	Précision : Le système recommande des packages pertinents avec un score satisfaisant (Precision@5>0.7).
•	Cohérence : Le système comprend et traduit correctement plus de 80% des requêtes en langage naturel.
•	Opérabilité : Le projet est entièrement documenté, reproductible et déployable.
•	Pertinence : Le projet est présentable comme une démonstration de compétences solides en Data Science et en IA générative.
Analyse des Risques :
•	Faible qualité des données : Risque que les données publiques soient insuffisantes ou de mauvaise qualité. Atténuation : Combiner plusieurs sources ou générer des données synthétiques.
•	Mauvaise interprétation du LLM : Le modèle pourrait mal interpréter des requêtes complexes ou ambiguës. Atténuation : Mettre en place un plan de tests robuste et affiner le prompt engineering.
•	Complexité de l'intégration : L'interconnexion de tous les modules peut être complexe. Atténuation : Adopter une approche de développement modulaire et tester chaque composant séparément.
________________________________________
## 8. Livrables attendus
•	Code source documenté sur GitHub.
•	API REST fonctionnelle.
•	Interface utilisateur interactive.
•	Documentation technique complète.
•	Rapport final / Blog technique expliquant la méthodologie et les résultats.
•	Vidéo de démonstration (2-3 minutes).
________________________________________
## 9. Valeur ajoutée
•	Pour le marché : Soutien à la digitalisation du tourisme et amélioration de l'engagement client en Tunisie et en Europe.
•	Pour l'étudiant : Projet complet démontrant des compétences "end-to-end" en ingénierie des données, machine learning, NLP, API et développement d'interface utilisateur.

