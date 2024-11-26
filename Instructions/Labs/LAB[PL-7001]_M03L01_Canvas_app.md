---
lab:
  title: "Labo 3\_: Créer une application de canevas"
  module: 'Module 3: Customize a canvas app in Power Apps'
---

# Labo de pratique 3 : Créer une application canevas

Dans ce labo, vous allez concevoir et créer une application canevas à partir de rien, ajouter une source de données et une galerie.

## Contenu du didacticiel

- Comment créer une application canevas avec une galerie liée à une source de données
- Comment mettre en forme des champs avec des formules Power Fx

## Étapes de labo de haut niveau

- Créer une application canevas à partir de zéro
- Ajouter une source de données à l’application
- Ajouter une galerie à l’application
- Configurer les champs dans la galerie
  
## Prérequis

- Doit avoir complété le **Labo 2 : Modèle de données**

## Procédure détaillée

## Exercice 1 : Créer une application canevas

### Tâche 1.1 : Créer l’application

1. Accédez au portail de création Power Apps `https://make.powerapps.com`

1. Vérifiez que vous êtes dans l’environnement **Dev One**.

1. Sélectionnez l’onglet **+ Créer** dans le menu de navigation de gauche.

1. Sélectionner la **vignette de l’application vide** sous **Démarrer depuis**.

1. Sélectionner **Créer** sous la vignette **application de canevas vide**.

    ![Capture d’écran de création à partir du vide.](../media/create-from-blank.png)

1. Entrer `Booking Request app` pour le **Nom de l’application**.

1. Sélectionner **Tablette** pour **Format**.

    ![Capture d’écran du nouveau nom de l’application.](../media/app-name-format.png)

1. Sélectionnez **Créer**.

1. Attendre que l’application soit générée.

1. Sélectionner **Enregistrer** en haut à droite de Power Apps Studio.


### Tâche 1.2 : Ajouter une source de données

1. Dans le menu de création d’applications, sélectionnez **Données**.

    ![Capture d’écran du volet de données.](../media/studio-data-pane.png)

1. Sélectionner le menu déroulant en à côté d’**Ajouter des données** et entrer `Booking` dans **Rechercher**.

    ![Capture d’écran de la sélection de la source de données.](../media/studio-data-search.png)

1. Sélectionner la table **Requêtes de réservation** Microsoft Dataverse.


### Tâche 1.3 : Configurer l’écran principal

1. Dans le menu création d’application, sélectionner **Arborescence**.

1. Sélectionnez **Screen1** dans l’arborescence, sélectionnez les points de suspension (**...**), puis sélectionnez **Renommer**.

1. Saisissez `MainScreen`.

1. Dans le menu de création d’application, sélectionner **Insérer (+)**.

1. Insérer un **Rectangle**.

1. Faire glisser le rectangle vers le haut à gauche de l’écran.

1. Dans le menu création d’application, sélectionner **Arborescence**.

1. Renommez le rectangle par `HeaderRect`.

1. Définissez les propriétés du rectangle dans la barre de formule de la façon suivante :

   1. X = `0`
   1. Y = `0`
   1. Hauteur = `80`
   1. Largeur = `Parent.Width`

1. Dans le menu de création d’application, sélectionner **Insérer (+)**.

1. Sélectionnez **Libellé de texte**.

1. Faire glisser l'étiquette vers le coin supérieur droit de l'écran.

1. Dans le menu création d’application, sélectionner **Arborescence**.

1. Donnez le nom `HeaderLabel` au contrôle Libellé de texte.

1. Définissez les propriétés de l’étiquette dans la barre de formule de la façon suivante :

   1. X = `0`
   1. Y = `0`
   1. Hauteur = `80`
   1. Largeur = `Parent.Width`
   1. Aligner = `Align.Center`
   1. Taille = `24`
   1. Texte = `"Booking Request"`
   1. Couleur = `Color.White`

    ![Capture d'écran de l'écran principal avec en-tête.](../media/main-screen.png)

1. Sélectionner **Enregistrer** en haut à droite de Power Apps Studio.


### Tâche 1.4 : Ajouter une galerie

1. Dans le menu de création d’application, sélectionner **Insérer (+)**.

1. Sélectionnez **Galerie verticale**.

    ![Capture d’écran de l’ajout d’une galerie.](../media/add-gallery.png)

1. Sélectionnez **Booking Requests** comme source de données.

    ![Capture d’écran des propriétés de la galerie.](../media/gallery-properties.png)

1. Sous l’onglet **Propriétés**, pour **Mise en page**, sélectionnez **Titre, sous-titre et corps**.

1. Choisissez **7 sélectionnés** en regard de **Champs**.

1. Sélectionnez **Cost** pour **Body1**.

1. Sélectionnez **Decision** pour **Subtitle2**.

1. Sélectionnez **Pet Name** pour **Title2**.

    ![Capture d’écran des champs de la galerie.](../media/select-fields.png)

1. Fermez le volet **Données**.

1. Dans le menu création d’application, sélectionner **Arborescence**.

1. Donnez le nom `BookingRequestList` à la galerie.

1. Définissez les propriétés de la galerie dans la barre de formule de la façon suivante :

   1. X = `0`
   1. Y = `80`
   1. Hauteur = `575`
   1. Largeur = `250`


### Tâche 1.5 : Mettre en forme le champ des devises

1. Dans le menu création d’application, sélectionner **Arborescence**.

1. Développez la galerie **BookingRequestList**.

1. Sélectionnez **Body1**.

    ![Capture d’écran du champ de corps sélectionné.](../media/body.png)

1. Définissez la propriété **Text** dans la barre de formule sur la formule :

    ```powerappsfl
    Text(Value(ThisItem.Cost), "$#,##0.00")
    ```

1. Sélectionner **Enregistrer** en haut à droite de Power Apps Studio.

1. Sélectionner le bouton **<- Précédent** en haut à gauche de la barre de commandes, puis sélectionner **Quitter** pour quitter l’application.

