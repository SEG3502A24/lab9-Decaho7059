
# Temperature Converter - SEG 3502 Lab 9

**Auteur :** Gbegbe Decaho  
**Numéro étudiant :** 300094197  
**Cours :** SEG 3502 - Laboratoire 9  

---

## Description du projet

Ce projet est une application Web permettant la conversion de températures, développée dans le cadre du laboratoire 9 du cours SEG 3502. Il utilise **Spring Boot** et inclut une gestion des utilisateurs et une sécurisation par authentification de base (*Basic Authentication*).

L'application prend en charge l'authentification en mémoire avec trois utilisateurs différents, chacun ayant un rôle défini. Le projet a été conçu pour être exécuté localement.

---

## Fonctionnalités

1. **Conversion de températures** :
   - Convertit les températures entre Celsius, Fahrenheit et Kelvin.
   
2. **Authentification en mémoire** :
   - Trois utilisateurs configurés :
     - `appuser` / `userpassword`
     - `user1` / `pass1`
     - `user2` / `pass2`
   
3. **Sécurité via Spring Security** :
   - Accès restreint : toutes les requêtes nécessitent une authentification.
   - Connexion via HTTP Basic.

4. **Interface utilisateur minimaliste** :
   - Page de connexion personnalisée (accessible via `/login`).

---

## Exécution locale

### Prérequis

- **Java 17** ou une version plus récente installée.
- **Gradle** installé (ou utilisation de Gradle Wrapper intégré).
- Navigateur Web pour tester l'application.

### Étapes d'exécution

1. Clonez le projet depuis le dépôt GitHub :
   ```bash
   git clone https://github.com/stephanesome/tempconverter-security.git
   ```
2. Naviguez dans le répertoire du projet :
   ```bash
   cd tempconverter
   ```
3. Lancez l'application avec la commande suivante :
   ```bash
   ./gradlew bootRun
   ```
4. Une fois l'application démarrée, ouvrez votre navigateur et accédez à :
   [http://localhost:8080](http://localhost:8080)

---

## Utilisateurs de test

| **Nom d'utilisateur** | **Mot de passe** | **Rôle** |
|------------------------|------------------|----------|
| `appuser`             | `userpassword`  | `USER`   |
| `user1`               | `pass1`         | `USER`   |
| `user2`               | `pass2`         | `USER`   |

**Remarque** : Assurez-vous d'utiliser les informations d'identification correctes lors de la connexion pour accéder aux fonctionnalités.

---

## Structure du projet

- **`src/main/java/seg3x02/converter`** :
  Contient les fichiers source principaux de l'application, notamment :
  - `WebSecurityConfig` : Configuration de Spring Security (authentification et utilisateurs).
  - `TemperatureController` : Gestionnaire des endpoints de conversion de température.
  
- **`src/main/resources/templates`** :
  Contient les fichiers HTML, y compris la page de connexion.

- **`src/main/resources/static`** :
  Contient les fichiers statiques tels que CSS et JS.

---

## Lien GitHub du professeur

- [tempconverter-security](https://github.com/stephanesome/tempconverter-security.git)

---

## Problèmes connus

- Assurez-vous que le port `8080` est disponible avant d'exécuter l'application.
- Cette application est une démonstration pédagogique et n'inclut pas de sécurité avancée ou de base de données.

---

## Auteur

**Nom :** Gbegbe Decaho  
**Numéro étudiant :** 300094197  
