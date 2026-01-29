# 🦷 DentalFlow
## Plateforme DevSecOps pour la gestion de prothèses dentaires

DentalFlow est une application web orientée **DevSecOps** dédiée à la gestion des commandes de prothèses dentaires.  
Le projet intègre des exigences fortes de **traçabilité réglementaire**, de **sécurité** et de **qualité logicielle**, conformément aux contraintes du domaine médical.

L’application repose sur une architecture **frontend / backend conteneurisée**, avec l’intégration d’outils de **qualité**, de **sécurité** et d’**observabilité** tels que **SonarQube**, **Swagger (OpenAPI)** et **Spring Boot Actuator**.

---

## 📑 Sommaire

- 🎯 Objectifs
- 🧱 Architecture globale
- 🚀 Stack technique
- 🔐 Sécurité & conformité (RGPD / Security by Design)
- 📦 Lancement du projet
- 📊 Qualité du code & DevSecOps
- 📘 Documentation technique
- 🐳 Docker & conteneurisation
- 🔁 CI/CD (prévu)
- 🛣️ Évolutions prévues
- 👤 Auteur

---

## 🎯 Objectifs

- Gérer les commandes de prothèses dentaires
- Assurer la **traçabilité réglementaire** (RDM)
- Minimiser et sécuriser les **données patients**
- Mettre en place une **chaîne DevSecOps complète**
- Fournir une base technique **propre, maintenable et auditable**

---

## 🧱 Architecture globale

```text
DentalFlow
├── frontend/            # Application frontend
├── backend/
│   └── dentalflow-app/  # Application Spring Boot
├── docker-compose.yml
├── nginx.conf
└── README.md
```
## Vue d’ensemble:

Frontend : application web servie via Nginx

Backend : API REST Spring Boot

Reverse proxy : Nginx

Qualité & sécurité : SonarQube

Observabilité : Spring Boot Actuator

Documentation API : Swagger / OpenAPI

## 🚀 Stack technique Backend

- Java 21

- Spring Boot 4.x

- Spring Web

- Spring Data JPA

- Spring Security

- Spring Boot Actuator

- Swagger / OpenAPI

- Maven (wrapper mvnw)

## Frontend

- Node.js

- Framework frontend : React / Next.js (selon implémentation)

- Nginx (serving + reverse proxy)

## DevSecOps

- Docker / Docker Compose

- SonarQube

- Git

## 🔐 Sécurité & conformité (RGPD / Security by Design)
- Données traitées

- Données patients minimisées

- Fichiers STL (modèles de prothèses)

- Base légale

- Obligation légale (RDM)

- Consentement du patient

- Conservation des données

- Archivage : 10 ans (exigences RDM)

- Principes de sécurité

- Security by Design

- Séparation claire des responsabilités

- Configuration externalisée

- Secrets non versionnés

- Images Docker minimales

## 📦 Lancement du projet Prérequis

- Docker & Docker Compose

- Node.js

- Java 21

- Lancement global
- docker-compose up --build

## Accès aux services

Frontend : http://localhost

Backend API : http://localhost:8080

Swagger : http://localhost:8080/swagger-ui.html

Actuator : http://localhost:8080/actuator

SonarQube : http://localhost:9000

## 📊 Qualité du code & DevSecOps

Le projet est analysé via SonarQube afin d’identifier :

- Bugs

- Code smells

- Vulnérabilités

- Dette technique

### Analyse frontend
npx sonar-scanner

### Analyse backend
./mvnw clean verify sonar:sonar

## 📘 Documentation technique
### 🧩 Backend – Architecture

- Architecture en couches

- Controller : exposition REST

- Service : logique métier

- Repository : accès aux données

## 📑 Swagger / OpenAPI

Swagger est utilisé pour :

- Documenter l’API

- Tester les endpoints

- Faciliter l’intégration frontend

### Accès :

/swagger-ui.html

### 📈 Spring Boot Actuator

Spring Boot Actuator permet :

- Monitoring applicatif

- Health checks

- Exposition de métriques techniques

Endpoints clés :

/actuator/health

/actuator/info

## 🐳 Docker & conteneurisation Backend

- Image Java slim

- Build multi-stage

- JAR Spring Boot

### Frontend:

- Build Node.js

- Image Nginx alpine

### Avantages:

- Images légères

- Déploiement reproductible

- Isolation des services

## 🔁 CI/CD

Le projet a intégré une chaîne CI/CD DevSecOps complète :

- Lint & tests automatiques

- Analyse SonarQube bloquante (Quality Gate)

- Build Docker automatisé

- Dependabot

- Déploiement contrôlé

### Outils envisagés:

- GitHub Actions / GitLab CI

- Docker

- SonarQube

## 🛣️ Évolutions prévues

- Authentification (JWT / OAuth2)

- Gestion fine des rôles

- Sécurisation HDS

- Tests de sécurité automatisés

## 👤 Auteur

Projet réalisé dans une démarche DevSecOps, orientée qualité, sécurité et maintenabilité, grâce à @Mister-deal, @Julien2195 et @leobelg.
Supervisé par 2I_ACADEMY