---
lab:
  title: "Labo\_2\_: Modèle de données"
  module: 'Module 2: Get started with Microsoft Dataverse'
---

# Labo pratique 2 : Modèle de données

Dans ce labo, vous allez créer des tables et des colonnes Dataverse.

## Contenu du didacticiel

- Comment créer des tables et des colonnes dans Microsoft Dataverse
- Comment créer une relation avec une colonne de recherche

## Étapes de labo de haut niveau

- Créer une table personnalisée
- Ajouter des colonnes à la table
- Créer une relation en utilisant une colonne de recherche
  
## Prérequis

- Vous devez avoir effectué le **Labo 0 : Valider l’environnement de labo**

## Procédure détaillée

## Exercice 1 – Créer des tables personnalisées

### Tâche 1.1 – Créer la table Booking Request (Demande de réservation)

1. Accédez au portail de création Power Apps `https://make.powerapps.com`

1. Vérifiez que vous êtes dans l’environnement **Dev One**.

1. Dans le volet de navigation de gauche, sélectionnez **Tables**.

1. Sélectionnez **+ Nouvelle table**, puis sélectionnez **Ajouter des colonnes et des données**.

    ![Capture d’écran de la création d’une table dans Dataverse.](../media/create-new-table-dataverse.png)

1. Sélectionnez l’icône de crayon **Modifier les propriétés de la table** en regard de **Nouvelle table**.

    ![Capture d’écran du nom de la nouvelle table.](../media/table-name.png)

1. Entrez `Booking Request` comme **Nom d’affichage**.

1. Sélectionnez **Enregistrer**.

### Tâche 1.2 : Colonne principale

1. Sélectionnez le caret déroulant en regard de **Nouvelle colonne**, puis sélectionnez **Modifier la colonne**.

    ![Capture d’écran de la colonne principale.](../media/primary-column.png)

1. Entrez `Pet Name` comme **Nom d’affichage**.

1. Sélectionnez **Mettre à jour**.

1. Sélectionnez **Créer**.

### Tâche 1.3 – Ajouter des colonnes

1. Dans le volet **Colonnes et données de Booking Request**, sélectionnez **+** pour ajouter une nouvelle colonne.

    ![Capture d’écran du volet de données.](../media/data-pane.png)

1. Dans le volet **Nouvelle colonne**, entrez ou sélectionnez les valeurs suivantes :

   1. Nom d’affichage : `Owner Name`
   1. Type de données : **Ligne de texte unique**
   1. Obligatoire : **Contrainte obligatoire**

    ![Capture d’écran du volet Nouvelle colonne.](../media/new-column-pane.png)

1. Sélectionnez **Enregistrer**.

1. Dans le volet **Colonnes et données de Booking Request**, sélectionnez **+** pour ajouter une nouvelle colonne.

1. Dans le volet **Nouvelle colonne**, entrez ou sélectionnez les valeurs suivantes :

   1. Nom d’affichage : `Owner Email`
   1. Type de données : **Ligne de texte unique**
   1. Format: **E-mail**
   1. Obligatoire : **Contrainte obligatoire**

1. Sélectionnez **Enregistrer**.

1. Dans le volet **Colonnes et données de Booking Request**, sélectionnez **+** puis, dans le volet **Nouvelle colonne**, entrez ou sélectionnez les valeurs suivantes :

   1. Nom d’affichage : `Start Date`
   1. Type de données : **Date et heure**
   1. Obligatoire : **Contrainte obligatoire**

1. Sélectionnez **Enregistrer**.

1. Dans le volet **Colonnes et données de Booking Request**, sélectionnez **+** puis, dans le volet **Nouvelle colonne**, entrez ou sélectionnez les valeurs suivantes :

   1. Nom d’affichage : `End Date`
   1. Type de données : **Date et heure**
   1. Obligatoire : **Facultatif**

1. Sélectionnez **Enregistrer**.

1. Dans le volet **Colonnes et données de Booking Request**, sélectionnez **+** puis, dans le volet **Nouvelle colonne**, entrez ou sélectionnez les valeurs suivantes :

   1. Nom d’affichage : `Cost`
   1. Type de données : **Devise**
   1. Obligatoire : **Facultatif**

1. Sélectionnez **Enregistrer**.

1. Dans le volet **Colonnes et données de Booking Request**, sélectionnez **+** puis, dans le volet **Nouvelle colonne**, entrez ou sélectionnez les valeurs suivantes :

   1. Nom d’affichage : `Notes`
   1. Type de données : **Plusieurs lignes de texte**
   1. Format: **Texte**
   1. Obligatoire : **Facultatif**

1. Sélectionnez **Enregistrer**.

### Tâche 1.4 : Ajouter une colonne de choix

1. Dans le volet **Colonnes et données de Booking Request**, sélectionnez **+** puis, dans le volet **Nouvelle colonne**, entrez ou sélectionnez les valeurs suivantes :

   1. Nom d’affichage : `Decision`
   1. Type de données : **Choix**
   1. Obligatoire : **Facultatif**

1. Sélectionnez **Non** pour **Synchroniser avec le choix global ?**

1. Entrez `Undecided` pour **Étiquette** et `1` pour **Valeur**.

1. Sélectionnez **+ Nouveau choix**, puis entrez `Accepted` pour **Étiquette** et `2` pour **Valeur**.

1. Sélectionnez **+ Nouveau choix**, puis entrez `Declined` pour **Étiquette** et `3` pour **Valeur**.

1. Sélectionnez **Undecided** (Indécis) pour **Choix par défaut**.

    ![Capture d’écran du volet Nouvelle colonne de choix.](../media/new-local-choice.png)

1. Sélectionnez **Enregistrer**.

## Exercice 2 : Créer une relation

### Tâche 2.1 : Créer une colonne de recherche

1. Accédez au portail de création Power Apps `https://make.powerapps.com`

1. Vérifiez que vous êtes dans l’environnement **Dev One**.

1. Dans le volet de navigation de gauche, sélectionnez **Tables**.

1. Sélectionnez **Booking Request**.

1. Dans le volet **Colonnes et données de Booking Request**, sélectionnez **+** puis, dans le volet **Nouvelle colonne**, entrez ou sélectionnez les valeurs suivantes :

   1. Nom d’affichage : `Account`
   1. Type de données : **Lookup**
   1. Obligatoire : **Facultatif**
   1. Table associée : **Compte**

    ![Capture d’écran du volet Nouvelle colonne de recherche.](../media/new-lookup.png)

1. Sélectionnez **Enregistrer**.

## Exercice 3 : Données

### Tâche 3.1 : Ajouter des enregistrements de demande de réservation

1. Accédez au portail Power Apps Maker <https://make.powerapps.com>.

1. Vérifiez que vous êtes dans l’environnement **Dev One**.

1. Dans le volet de navigation de gauche, sélectionnez **Tables**.

1. Sélectionnez **Booking Request**.

1. Dans le volet **Colonnes et données de Booking Request**, sélectionnez l’icône de menu déroulant à côté de **Modifier** et sélectionnez **Modifier dans un nouvel onglet**.

1. Entrez ou sélectionnez les valeurs suivantes :

   1. Pet Name: `Fido`
   1. Nom du propriétaire : `MOD Administrator`
   1. E-mail du propriétaire : Utiliser l’e-mail de votre locataire
   1. Date de début : **Demain**
   1. Date de fin : **Choisir une date de la semaine suivante**
   1. Cost : `1,000`
   1. Décision : **Accepted**

1. Sélectionnez **Insérer une ligne ci-dessous**, puis entrez ou sélectionnez les valeurs suivantes :

   1. Pet Name : `Tom`
   1. Nom du propriétaire : `MOD Administrator`
   1. E-mail du propriétaire : Utiliser l’e-mail de votre locataire
   1. Date de début : **Choisir une date du mois suivant**
   1. Date de fin : **Choisir une date après la date de début**
   1. Cost : `1,500`
   1. Décision : **Undecided**

1. Sélectionnez **Insérer une ligne ci-dessous**, puis entrez ou sélectionnez les valeurs suivantes :

   1. Pet Name : `Jim`
   1. Nom du propriétaire : `MOD Administrator`
   1. Owner Email : Utiliser l’e-mail de votre locataire
   1. Date de début : **Choisir une date future dans le mois en cours**
   1. Date de fin : **Choisir une date après la date de début**
   1. Cost : `250`
   1. Décision : **Declined**

1. Fermez l’onglet Modifier les données.

