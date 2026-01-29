# dentalFlow-DevSecOps

Présentation du projet

DentalFlow est une application web orientée DevSecOps destinée à la gestion des commandes de prothèses dentaires, intégrant des exigences fortes de traçabilité réglementaire, de sécurité et de qualité logicielle.

Le projet est conçu selon une architecture frontend / backend conteneurisée, avec une intégration d’outils de qualité et de sécurité comme SonarQube, Swagger et Spring Boot Actuator.

🎯 Objectifs

Gérer les commandes de prothèses dentaires

Assurer la traçabilité réglementaire (RDM)

Minimiser et sécuriser les données patients

Mettre en place une chaîne DevSecOps complète

Fournir une base technique propre, maintenable et auditable

🧱 Architecture globale

DentalFlow
├── frontend/            # Application frontend
├── backend/
│   └── dentaflow-app/   # Application Spring Boot
├── docker-compose.yml
├── nginx.conf
└── README.md

Vue d’ensemble

Frontend : application web servie via Nginx

Backend : API REST Spring Boot

Reverse proxy : Nginx

Qualité & sécurité : SonarQube

Observabilité : Actuator

API DOC: Swagger

🚀 Stack technique

Backend

Java 21

Spring Boot 4.x

Spring Web

Spring Data JPA

Spring Security (prévu)

Spring Boot Actuator

Swagger / OpenAPI

Maven (wrapper mvnw)

Frontend

Node.js

Framework frontend (React / Next.js selon implémentation)

Nginx (serving + reverse proxy)

DevSecOps

Docker / Docker Compose

SonarQube

Git

🔐 Sécurité & conformité

Données traitées

Données patients minimisées

Fichiers STL (prothèses)

Base légale

Obligation légale (RDM)

Consentement

Conservation

Archivage : 10 ans (RDM)

📦 Lancement du projet

Prérequis

Docker & Docker Compose

Node.js

Java 21

Lancement global

docker-compose up --build

Accès aux services

Frontend : http://localhost

Backend API : http://localhost:8080

Swagger : http://localhost:8080/swagger-ui.html

Actuator : http://localhost:8080/actuator

SonarQube : http://localhost:9000

📊 Qualité du code (SonarQube)

Le projet est analysé via SonarQube pour :

Bugs

Code smells

Vulnérabilités

Dette technique

Analyse frontend :

npx sonar-scanner

Analyse backend :

./mvnw clean verify sonar:sonar

📘 Documentation technique

🧩 Backend – Architecture

Pattern

Architecture en couches

Controller

Service

Repository

Responsabilités

Controller : exposition REST

Service : logique métier

Repository : accès aux données

📑 Swagger / OpenAPI

Swagger est utilisé pour :

Documenter l’API

Tester les endpoints

Faciliter l’intégration frontend

Accès :

/swagger-ui.html

📈 Actuator

Spring Boot Actuator permet :

Monitoring applicatif

Health checks

Metrics techniques

Endpoints clés :

/actuator/health
/actuator/info

🐳 Docker

Backend

Image Java slim

Build multi-stage

Jar Spring Boot

Frontend

Build Node

Image Nginx alpine

Avantages

Images légères

Déploiement reproductible

Isolation des services

🔄 Bonnes pratiques DevSecOps

Analyse SonarQube systématique

Séparation front / back

Configuration externalisée

Tokens et secrets non versionnés

Images Docker minimales

🛣️ Évolutions prévues

Authentification (JWT / OAuth2)

Gestion fine des rôles

Sécurisation HDS

CI/CD (GitHub Actions / GitLab CI)

Tests de sécurité automatisés

👤 Auteur

Projet réalisé dans une démarche DevSecOps, orientée qualité, sécurité et conformité réglementaire.
