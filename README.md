# Partie 1 du projet
Installation de la base de données et exercices SQL

## Instructions d'installation
### Installer la base de données en utilisant le fichier script.sql.
## Exercices SQL
### Une fois la base de données installée, réalisez les exercices suivants :

### 1 Sélectionner toutes les informations des comptes
Sélectionner toutes les colonnes du compte ayant l'ID 3.

### 2 Comptes avec solde inférieur à 600
Sélectionner toutes les colonnes des comptes avec un solde disponible strictement inférieur à 600.

### 3 Comptes d'épargne avec solde inférieur à 600
Sélectionner toutes les colonnes des comptes d'épargne avec un solde disponible strictement inférieur à 600.

### 4 Comptes ouverts en décembre 2004
Afficher toutes les colonnes des comptes ouverts entre le 1er décembre 2004 et le 30 décembre 2004.

### 5 Employés du département 3
Afficher les prénoms et noms des employés du département 3, triés par ordre alphabétique selon le prénom.

### 6 Comptes ouverts le 12 mars 2001
Afficher les numéros des employés ayant ouvert des comptes le 2001-03-12.

### 7 Comptes-titres avec solde supérieur à 6000
Afficher les comptes-titres avec un solde disponible supérieur à 6000.

### 8 Adresse du quartier général
Afficher l'adresse, le code postal et la ville du quartier général de l'entreprise.

### 9 Postes des employés sans doublons
Afficher les différents noms de postes des employés, sans doublons.

### 10 Nom de produit du compte 14
Afficher le nom de produit associé au compte 14.

### 11 Directeurs avec nom de famille commençant par C
Afficher les noms et prénoms des directeurs ayant un nom de famille commençant par la lettre C.

### 12 Comptes liés aux prêts pour petites entreprises
Afficher tous les comptes en lien avec des prêts pour les petites entreprises.

### 13 Somme des soldes des comptes ouverts par Paula Roberts
Afficher la somme des soldes disponibles des comptes ouverts par l'employée Paula Roberts.

### 14 Transactions cumulatives par compte
Calculer le montant total des transactions (crédits et débits) pour chaque compte sur une période donnée.

### 15 Clients avec plusieurs types de comptes
Trouver les clients qui ont à la fois un compte courant et un compte d'épargne.

# Partie 2 du projet

## ⚠️ Attention, des erreurs ont été volontairement ajoutées. À vous de les trouver. 

Dans cette deuxième partie du projet, votre tâche consistera à créer des cas de test fonctionnels pour l'API et à les exécuter à l'aide de l'outil Postman. Voici un aperçu de ce que vous devez accomplir dans cette étape :

### Étape 1 : 
Réalisez vos cas de test
Dans cette étape, vous devrez concevoir et créer des scénarios de test qui couvrent différents aspects et fonctionnalités de l'API que vous souhaitez évaluer. Assurez-vous de prendre en compte les différents cas d'utilisation, les entrées possibles et les conditions de réussite pour chaque cas de test. Documentez soigneusement vos cas de test, y compris les étapes à suivre, les données d'entrée nécessaires et les attentes de sortie. Cette étape est essentielle pour garantir une évaluation complète de l'API.

### Étape 2 : 
Utilisez Postman pour tester l'API
Après avoir créé vos cas de test, vous utiliserez l'outil Postman pour exécuter ces scénarios sur l'API. Postman vous permettra d'envoyer des requêtes HTTP aux points d'extrémité de l'API, de fournir les données d'entrée nécessaires et de vérifier les réponses de l'API par rapport à vos attentes. Assurez-vous de noter les résultats de chaque test, enregistrant les succès et les échecs, ainsi que toute anomalie ou problème rencontré.

L'objectif de cette étape est d'identifier les éventuels problèmes, erreurs ou anomalies dans l'API, et de s'assurer que toutes les fonctionnalités sont correctement implémentées et fonctionnent comme prévu.

En résumé, dans la partie 2 du projet, vous serez chargé de créer des cas de test exhaustifs pour l'API et de les exécuter à l'aide de Postman pour évaluer sa qualité et sa conformité aux spécifications.

# documentation :

## Documentation de l'API de Gestion des Produits
Base URL
L'URL de base de l'API est l'adresse où votre script PHP est hébergé, par exemple : http://localhost/api/product_manager.php.

Méthodes HTTP et Endpoints
Création d'un Produit (Create)

## Méthode HTTP : POST
Endpoint : /api/product_manager.php
Body (application/x-www-form-urlencoded) :
product_cd (String) : Code du produit
name (String) : Nom du produit
product_type_cd (String) : Type de produit
date_offered (Date, format YYYY-MM-DD) : Date d'offre du produit
Lecture des Produits (Read)

## Méthode HTTP : GET
Endpoint : /api/product_manager.php
Mise à Jour d'un Produit (Update)

## Méthode HTTP : PUT
Endpoint : /api/product_manager.php
Body (application/x-www-form-urlencoded) :
product_cd (String) : Code du produit à mettre à jour
name (String) : Nouveau nom du produit
Suppression d'un Produit (Delete)

## Méthode HTTP : DELETE
Endpoint : /api/product_manager.php
Body (application/x-www-form-urlencoded) :
product_cd (String) : Code du produit à supprimer
Réponses de l'API
Succès : L'API retournera un message de succès pour l'opération effectuée, par exemple, "Nouveau produit créé avec succès" pour une création réussie.
Erreur : En cas d'erreur, l'API renverra un message d'erreur détaillé.
Exemples d'Utilisation

## Pour créer un produit :

curl -X POST http://localhost/api/product_manager.php \
-d "product_cd=PRD001&name=Produit+1&product_type_cd=Type1&date_offered=2022-01-01"

## Pour lire les produits :

curl -X GET http://localhost/api/product_manager.php

## Pour mettre à jour un produit :

curl -X PUT http://localhost/api/product_manager.php \
-d "product_cd=PRD001&name=Nouveau+Nom+Produit"

## Pour supprimer un produit :

curl -X DELETE http://localhost/api/product_manager.php \
-d "product_cd=PRD001"
Sécurité
Cette API ne comprend pas de mécanismes d'authentification ou de validation avancée. Il est fortement recommandé d'ajouter des couches de sécurité supplémentaires pour une utilisation en production.


## Documentation de l'API de Gestion des Employés

### URL de Base :
http://localhost/api/employee_manager.php.

Endpoints et Méthodes HTTP
Création d'un Employé (Create)

## Méthode HTTP : POST
Endpoint : /api/employee_manager.php
Body (JSON) :
json
Copy code
{
  "first_name": "Prénom",
  "last_name": "Nom",
  "start_date": "YYYY-MM-DD",
  "end_date": "YYYY-MM-DD",
  "title": "Titre",
  "assigned_branch_id": 123,
  "dept_id": 123,
  "superior_emp_id": 123
}
Lecture des Employés (Read)

## Méthode HTTP : GET
Endpoint : /api/employee_manager.php
Mise à Jour d'un Employé (Update)

## Méthode HTTP : PUT
Endpoint : /api/employee_manager.php
Body (JSON) :
json
Copy code
{
  "emp_id": 123,
  "first_name": "Nouveau Prénom",
  "last_name": "Nouveau Nom"
  // Ajouter d'autres champs si nécessaire
}
Suppression d'un Employé (Delete)

## Méthode HTTP : DELETE
Endpoint : /api/employee_manager.php
Body (JSON) :
json
Copy code
{
  "emp_id": 123
}
Format de Réponse
Succès : L'API retourne un message de succès pour l'opération effectuée, par exemple, "Nouvel employé créé avec succès" pour une création réussie.
Erreur : En cas d'erreur, l'API renvoie un message d'erreur détaillé.
Exemples d'Utilisation

## Pour créer un employé :

curl -X POST http://localhost/api/employee_manager.php \
-H "Content-Type: application/json" \
-d '{"first_name": "John", "last_name": "Doe", "start_date": "2023-01-01", "end_date": "2023-12-31", "title": "Manager", "assigned_branch_id": 1, "dept_id": 2, "superior_emp_id": 3}'

## Pour lire les employés :

curl -X GET http://localhost/api/employee_manager.php

## Pour mettre à jour un employé :

curl -X PUT http://localhost/api/employee_manager.php \
-H "Content-Type: application/json" \
-d '{"emp_id": 123, "first_name": "Jane", "last_name": "Smith"}'

## Pour supprimer un employé :

curl -X DELETE http://localhost/api/employee_manager.php \
-H "Content-Type: application/json" \
-d '{"emp_id": 123}'


## Documentation de l'API de Gestion des Clients
### URL de Base
http://localhost/api/customer_manager.php.

Endpoints et Méthodes HTTP
Création d'un Client (Create)

## Méthode HTTP : POST
Endpoint : /api/customer_manager.php
Body (JSON) :
json
Copy code
{
  "address": "Adresse",
  "city": "Ville",
  "cust_type_cd": "Type",
  "fed_id": "ID Fédéral",
  "postal_code": "Code Postal",
  "state": "État"
}
Lecture des Clients (Read)

## Méthode HTTP : GET
Endpoint : /api/customer_manager.php
Mise à Jour d'un Client (Update)

## Méthode HTTP : PUT
Endpoint : /api/customer_manager.php
Body (JSON) : Fonctionnalité non implémentée dans le script
Suppression d'un Client (Delete)

## Méthode HTTP : DELETE
Endpoint : /api/customer_manager.php
Body (JSON) :
json
Copy code
{
  "cust_id": 123
}
Format de Réponse
Succès : L'API retourne un message de succès pour l'opération effectuée.
Erreur : En cas d'erreur, l'API renvoie un message d'erreur détaillé.
Exemples d'Utilisation

## Pour créer un client :

curl -X POST http://localhost/api/customer_manager.php \
-H "Content-Type: application/json" \
-d '{"address": "123 Main St", "city": "Anytown", "cust_type_cd": "I", "fed_id": "123456789", "postal_code": "12345", "state": "State"}'

## Pour lire les clients :

curl -X GET http://localhost/api/customer_manager.php
Pour mettre à jour un client : Fonctionnalité non implémentée dans le script

## Pour supprimer un client :

curl -X DELETE http://localhost/api/customer_manager.php \
-H "Content-Type: application/json" \


*************************************************
# Exemple de Retours pour Chaque Appel à l'API
API de Gestion des Clients

## Création d'un Client (POST)

Réussite : "Nouveau client créé avec succès"
Échec : "Erreur: [Détails de l'erreur]"

## Lecture des Clients (GET)

Réussite : "ID: 1 - Ville: Paris<br>ID: 2 - Ville: Lyon<br>" (et ainsi de suite pour chaque client)
Échec : "0 résultat"

## Mise à Jour d'un Client (PUT)
Réponse Attendue :
Réussite : 
{
  "status": "success",
  "message": "Client mis à jour avec succès."
}
Échec : 
{
  "status": "error",
  "message": "Mise à jour des clients non implémentée."
}

## Suppression d'un Client (DELETE)

Réussite : "Client supprimé avec succès"
Échec : "Erreur de suppression: [Détails de l'erreur]"
API de Gestion des Employés

## Création d'un Employé (POST)

Réussite : "Nouvel employé créé avec succès"
Échec : "Erreur: [Détails de l'erreur]"

## Lecture des Employés (GET)

Réussite : "ID: 1 - Nom: John Doe<br>ID: 2 - Nom: Jane Smith<br>" (et ainsi de suite pour chaque employé)
Échec : "0 résultat"

## Mise à Jour d'un Employé (PUT)

Réussite : "Employé mis à jour avec succès"
Échec : "Erreur de mise à jour: [Détails de l'erreur]"

## Suppression d'un Employé (DELETE)

Réussite : "Employé supprimé avec succès"
Échec : "Erreur de suppression: [Détails de l'erreur]"
API de Gestion des Produits

## Création d'un Produit (POST)

Réussite : "Nouveau produit créé avec succès"
Échec : "Erreur: [Détails de l'erreur]"

## Lecture des Produits (GET)

Réussite : "Code du produit: PRD001 - Nom: Produit 1 - Type: Type1<br>Code du produit: PRD002 - Nom: Produit 2 - Type: Type2<br>" (et ainsi de suite pour chaque produit)
Échec : "0 résultat"

## Mise à Jour d'un Produit (PUT)

Réussite : "Produit mis à jour avec succès"
Échec : "Erreur de mise à jour: [Détails de l'erreur]"

## Suppression d'un Produit (DELETE)

Réussite : "Produit supprimé avec succès"
Échec : "Erreur de suppression: [Détails de l'erreur]"
-d '{"cust_id": 123}'
curl -X DELETE http://localhost/api/employee_manager.php \
-H "Content-Type: application/json" \
-d '{"emp_id": 123}'

