# TP 3 - Formulaires Symfony

## Description

Création d'un formulaire pour ajouter un produit au panier. Le formulaire permet de choisir la quantité et la couleur d'un casque audio.

### 1. Création du Form Type

**Fichier :** `src/Form/Type/ProductType.php`

J'ai créé un Form Type avec deux champs :
- **quantity** : un champ nombre (IntegerType) avec min=1 et max=10
- **color** : une liste déroulante (ChoiceType) avec 3 couleurs au choix

J'ai aussi activé la protection CSRF.

### 2. Création du Contrôleur

**Fichier :** `src/Controller/ProductController.php`

Le contrôleur gère la route `/product` et fait 3 choses :
- Créer le formulaire
- Récupérer les données quand on soumet le formulaire
- Envoyer le formulaire à la vue Twig

### 3. Création de la Vue

**Fichier :** `templates/product/index.html.twig`

La page affiche :
- L'image du produit
- Les informations (prix, description, caractéristiques)
- Le formulaire avec les fonctions Twig (form_start, form_widget, etc.)

### 4. Modification du Template de Base

**Fichier :** `templates/base.html.twig`

J'ai ajouté Bootstrap pour avoir un design correct.

## Ce que j'ai appris

- Comment créer un formulaire avec Symfony
- La différence entre IntegerType et ChoiceType
- Comment afficher un formulaire dans Twig
- Le pattern MVC (Model-View-Controller)
- Les commandes Git (add, commit, push)