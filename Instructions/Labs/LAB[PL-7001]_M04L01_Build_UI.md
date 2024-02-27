---
lab:
  title: "Labo\_4\_: Créer l’interface utilisateur"
  module: 'Module 4: How to build the UI in a canvas app in Power Apps'
---

# Atelier 4 : Créer l'interface utilisateur

Dans cet atelier, vous allez modifier les couleurs des contrôles dans l'application.

## Contenu du didacticiel

- Utilisation des thèmes
- Personnalisation de votre application

## Étapes de labo de haut niveau

- Sélectionner un thème
- Personnalisation
  
## Prérequis

- Vous devez avoir terminé **Labo 3 : Créer une application canevas**

## Procédure détaillée

## Exercice 1 – Thème

### Tâche 1.1 : Modifier l'application

1. Accédez au portail Power Apps Maker <https://make.powerapps.com>.

1. Vérifiez que vous êtes dans l’environnement **Dev One**.

1. Sélectionnez l’onglet **Applications** dans le menu de gauche.

1. Sélectionnez l'**application Booking Request**, sélectionnez les commandes (**...**), puis **Modifier > Modifier dans un nouvel onglet**.

### Tâche 1.2 : sélectionner un thème

1. Dans la barre d'actions de Power Apps Studio, sélectionnez **Thème**.

    ![Capture d'écran de Sélectionner les thèmes.](../media/select-theme.png)

1. Sélectionnez le thème **Rouge**.

### Tâche 1.3 : contrôles de marque

1. Dans le menu de création d'application, sélectionnez **Arborescence**.

1. Développez la galerie.

1. Sélectionnez **NextArrow**.

1. Définissez la propriété **Color** de NextArrow dans la barre de formule sur :

    ```powerappsfl
    RGBA(164, 38, 44, 1)
    ```

1. Sélectionnez **Corps**.

1. Définissez la propriété **Color** de Body dans la barre de formule sur :

    ```powerappsfl
    If(ThisItem.Cost > 1000, RGBA(164, 38, 44, 1), Color.Black)
    ```

1. Sélectionnez **Enregistrer** dans le coin supérieur droit de Power Apps Studio.

## Exercice 2 : Personnalisation

### Tâche 2.1 : Ajouter une étiquette utilisateur

1. Cliquez en dehors de la galerie sur le canevas vide.

1. Dans le menu de création d'application, sélectionnez **Insérer (+)**.

1. Sélectionnez **Libellé de texte**.

1. Faites glisser l'étiquette dans le coin supérieur droit de l'écran.

1. Dans le menu de création d'application, sélectionnez **Arborescence**.

1. Donnez le nom `UserLabel` au contrôle Libellé de texte.

1. Définissez les propriétés de l’étiquette dans la barre de formule de la façon suivante :

   1. X = `1100`
   1. Y = `20`
   1. Hauteur = `40`
   1. Largeur = `250`
   1. Aligner = `Align.Right`
   1. Taille = `18`
   1. PaddingRight = `10`
   1. Color = `Color.White`
   1. Texte = `User().FullName`

    ![Capture d'écran de l'écran principal avec personnalisation.](../media/main-screen-personalized.png)

1. Sélectionnez **Enregistrer** dans le coin supérieur droit de Power Apps Studio.

1. Sélectionner le bouton **<- Précédent** en haut à gauche de la barre de commandes, puis sélectionner **Quitter** pour quitter l’application.
