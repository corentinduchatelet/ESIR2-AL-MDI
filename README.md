# ESIR 2 TP AL
## Nicolas BOURDIN et Corentin DUCHATELET

Ceci est le rendu de notre TP de conception objet

#### TP1

Le premier exercice était l'implémentation du **Pattern Observer**.

Ici, la boite aux lettres prévient ses observeurs CounterObserver qui a pour but de compter le nombre de mail et MailObserver qui a pour but d'afficher les infos sur le mail.

#### TP2

Pour le TP2, qui ressemble au projet que nous avions eu en début d'année en COMPILATION (arbre de syntaxe abstraite), on utilise le **patron de conception Visiteur**.

On modifie les méthodes dans AbstractInterpretor pour créer un comportement à chaque bloc ou élément rencontré. Pour le pretty-printer, on met des tabulations là où il faut dans les blocs et l'imbrication se fait automatiquement, on peut d'ailleurs compter le niveau d'imbrication en ajoutant une fonction très simplement.

#### TP3

Pour le TP3, nous avons réfléchis sur les conceptions possibles du **Pattern Decorator et State**.

* Q1.Le diagramme était erronné sur plusieurs points:
-Pas de coordinateur

-Petite vs Grande pizza : Puisque qu'l n'y a pas de différence de comportement, il n'est pas nécessaire de créer une classe pour chaque type de pizza

-Gestion des état des commandes : patron de conception à état

-Pas de moyens pour le collaborateur de se signaler comme "disponible"

-la visibilité inutile dans un diagramme de classe

-certains rôles sont explicités mais inutiles


* Q2.Le pattern decorator est plus intéressant qu'un héritage simple car il permet d'ajouter des couches de paiements pour gérer plus aisément le paiement final de l'utilisateur

* Q3.Le pattern state permettra d'avoir différents comportements de nos classes en fonction de l'état de la pizza. En modifiant l'état de la commande (par le coordinateur), on aura donc une différente méthode appelée lorsqu'on l'appellera.

Chaque méthode des classes concrètes (propre au pattern) doit réaliser le traitement métier nécessaire avant de passer à l'état suivant.

Par la suite on pourra ajouter des états supplémentaires plus facilement dans le code sans changer les états déja mis en place puisque le comportement d'une commande est séparé des données

=>On pourrait utiliser le pattern Observer pour que le coordinateur "observe" les collaborateurs "observable" et puisse etre mis au courant de leur avancée


![Diagramme commande](https://raw.githubusercontent.com/corentinduchatelet/ESIR2-AL-MDI/master/diagramme_commande.jpg)

![Diagramme paiement](https://raw.githubusercontent.com/corentinduchatelet/ESIR2-AL-MDI/master/diagramme_pizza.jpg)
