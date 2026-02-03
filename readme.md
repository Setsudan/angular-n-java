# 📋 TaskFlow - Gestionnaire de Tâches Sécurisé

**TaskFlow** est un projet d'apprentissage Full Stack conçu pour maîtriser l'intégration entre **Angular**, **Spring Boot** et **PostgreSQL**.

L'objectif principal est de mettre en œuvre une architecture de sécurité robuste utilisant des **JWT stockés dans des Cookies HttpOnly** (pas de LocalStorage) et une gestion des rôles (RBAC) stricte.

---

## 🚀 Stack Technique

* **Frontend :** Angular (Standalone Components, Interceptors fonctionnels)
* **Backend :** Java Spring Boot (Spring Security 6, JPA/Hibernate)
* **Base de Données :** PostgreSQL
* **Infrastructure :** Docker & Docker Compose

## ✨ Fonctionnalités Clés

### 1. Sécurité Avancée

* **Authentification JWT :** Le token n'est jamais exposé au Typescript. Il est stocké dans un cookie `HttpOnly`, `Secure` et `SameSite`.
* **Angular Interceptor :** Utilisation de `withCredentials: true` pour attacher automatiquement le cookie aux requêtes API.
* **Guards :** Protection des routes Angular selon l'état de connexion.

### 2. Gestion des Rôles (RBAC)

* **Rôle MANAGER :** Peut voir toutes les tâches et en créer de nouvelles.
* **Rôle USER :** Ne voit que ses propres tâches et peut changer le statut à "COMPLETED".

Pour que je valide ton projet il faut que le projet se lance sur docker, que la configuration soit bien prise en compte.
Que le projet soit utilisable et qu'aucun bug ne soit bloquant. Les bugs visuel ou genant c'est ok