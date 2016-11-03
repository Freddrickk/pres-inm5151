class: center, middle

# Fuzzing as a service (FAAS)

##### Frédéric Vachon, Martin Grogan et Benjamin Rosa

---
# TODO : Plan de la présentation

---

# Fuzzing as a service (FAAS)

* Améliorer la qualité et la sécurité des logiciels pour les acteurs qui n'ont pas d'immense budget à investir

* Inciter les gens à intégrer le fuzzing dans le cycle du développement de leur logiciel

* Démocratiser la pratique du fuzzing

    * Produit gratuit

    * Facile d'utilisation

---

# Principales fonctionnalités

* Lancer des tâches de Fuzzing

* Consulter les tâches en cours

* Consulter les rapports de crash

* Fournir des fichiers d’entrée pour un programme donné


---

## Contenu des sprints


* Sprint 1
	* Préparer l’environnement de développement
	* L’utilisateur peut se connecter et se déconnecter de l’application
	* Le visiteur peut se créer un compte utilisateur 
	* L’utilisateur peut créer une tâche de fuzzing simplifiée ne contenant que le programme à tester

* Sprint 2

	* L’utilisateur peut démarrer une tâche de fuzzing en définissant une grammaire de base pour injecter des données dans un programme
	* L’utilisateur peut fuzzer un programme via l’entrée standard
	* L’utilisateur peut consulter la liste des rapports de crash
	* L’utilisateur peut consulter la liste des tâches de fuzzing

* Sprint 3
	* L’utilisateur peut consulter les détails d’un crash
	* L’utilisateur peut consulter les détails d’une tâche de fuzzing
	* L’utilisateur peut forcer l’arrêt d’une tâche de fuzzing

---

# Sprint backlog

* Préparer l’environnement de développement	
	* Créer un conteneur avec React JS et un serveur web :	6 heures	
	* Créer un conteneur avec Django pour l’API REST :	4 heures	
	* Créer un conteneur pour contenir la base de donnée :	4 heures	
	* Assembler les conteneurs en utilisant Docker-Compose :	1 heures	
	* Écrire la documentation :	1 heures	

* Se connecter et se déconnecter sur son compte utilisateur	
	* Front-end : implémenter l’écran d’interface permettant de se connecter à l’application :	5 heures	
	* UX : créer le design de l’écran de connection :	1 heures	
	* Back-end : créer le service d’authentification :	8 heures	
	* Écrire la documentation :	1 heures	

---

# Sprint backlog (suite)

* Créer un compte utilisateur	
	* UX: créer le design de l’écran de création de compte :	1 heures	
	* Front-end : implémenter l’écran de création de compte :	4 heures	
	* Back-end : créer le service de création de compte, créer une table utilisateur dans la base de donnée :	5 heures	
	* Écrire la documentation :	1 heures	

* Créer une tâche de fuzzing simplifié	
	* UX: créer le design de l’écran création de tâche de fuzzing :	1 heures	
	* Front-end : implémenter l’écran de création de tâche :	5 heures	
	* Back-end : créer le service de création de tâche, création d’une table tache dans la base de donnée :	8 heures	
	* Écrire la documentation :	1 heures	

---

# Créer une tâche simplifiée


1. L’utilisateur se trouve sur l’écran d’accueil de l’application et clique sur le bouton Task.
2. Le système retourne un écran contenant la liste des Task
3. L’utilisateur appuie sur le bouton Add task
4. Le système retourne l’écran de création de tâche
5. L’utilisateur entre les informations (nom, description) et téléverse un fichier binaire puis appuie sur le bouton ok
6. Le serveur valide les champs et crée une nouvelle tâche dans la base de donnée puis renvoie un code de succès
7. Le système affiche l’écran d’accueil

---

# Créer une tâche simplifiée

![](./img/creer_tache.png)

---

# Authentification

1. le Visiteur remplit les champs suivants et clique sur le bouton : 
 - Nom utilisateur
 - Mot de passe
2. Le système analyse la requête, cherche et trouve l’utilisateur dans la base de donnée et retourne les informations le concernant à l’interface web
3. le Visiteur devenu Utilisateur a maintenant accès à sa page personnelle.


![](./img/auth.png)

---

# Diagramme de classe d'une tâche

![](./img/task.png)

---

# TODO : Revue de sprint

---

# Plan du prochain sprint

1. En tant qu’utilisateur je peux démarrer une tâche de fuzzing en définissant une grammaire de base pour injecter des données dans un programme afin de pouvoir le tester à travers une série d’attaque de type brute force.

2. En tant qu’utilisateur je peux fuzzer un programme via l’entrée standard afin de pouvoir tester et détecter d’autres failles potentielles de mon programme.

3. En tant qu’utilisateur je peux consulter la liste des rapports de crash afin de pouvoir avoir rapidement un point de vue global sur les rapports émis par les tâches de fuzzing.

4. En tant qu’utilisateur je peux consulter la liste des tâches de fuzzing afin de pouvoir avoir rapidement un point de vue global sur les tâches créées ainsi que leurs statuts.

---

# TODO : Sprint backlog initial

---

# Démo
