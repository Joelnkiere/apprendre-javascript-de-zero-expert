# Module 15 : Switch

## Objectifs

À la fin de ce module, vous serez capable de :

- Utiliser switch
- Comparer switch et if
- Gérer plusieurs cas simplement

---

# Pourquoi switch ?

Lorsque plusieurs choix sont possibles.

Exemple :

- jours de la semaine
- menus
- rôles utilisateurs

---

# Syntaxe

```javascript
switch(valeur){

    case valeur1:
        break;

    case valeur2:
        break;

    default:
}
```

---

# Exemple

```javascript
let jour = 1;

switch(jour){

    case 1:
        console.log("Lundi");
        break;

    case 2:
        console.log("Mardi");
        break;

    default:
        console.log("Inconnu");

}
```

---

# Importance de break

Sans break :

```javascript
case 1:
    console.log("Lundi");

case 2:
    console.log("Mardi");
```

Les deux seront exécutés.

---

# Cas pratique : Notes

```javascript
let mention = "A";

switch(mention){

    case "A":
        console.log("Excellent");
        break;

    case "B":
        console.log("Très Bien");
        break;

    case "C":
        console.log("Bien");
        break;

    default:
        console.log("Non défini");

}
```

---

# Switch ou If ?

Utiliser switch lorsque :

- une seule variable
- plusieurs valeurs possibles

Utiliser if lorsque :

- plusieurs conditions complexes

---

# Projet : Menu Restaurant

```javascript
let choix = 2;

switch(choix){

    case 1:
        console.log("Pizza");
        break;

    case 2:
        console.log("Burger");
        break;

    case 3:
        console.log("Poulet");
        break;

    default:
        console.log("Choix invalide");

}
```

---

# Exercices

## Exercice 1

Créer un switch affichant les mois :

1 → Janvier

2 → Février

3 → Mars

---

## Exercice 2

Créer un switch affichant :

- Admin
- Modérateur
- Utilisateur

---

## Exercice 3

Créer un menu de calculatrice :

1 → Addition

2 → Soustraction

3 → Multiplication

4 → Division

---

# Corrigés

## Correction Exercice 1

```javascript
switch(mois){

    case 1:
        console.log("Janvier");
        break;

    case 2:
        console.log("Février");
        break;

}
```

---

## Correction Exercice 2

```javascript
switch(role){

    case "admin":
        console.log("Admin");
        break;

    case "moderateur":
        console.log("Modérateur");
        break;

}
```

---

## Correction Exercice 3

```javascript
switch(operation){

    case 1:
        console.log(a+b);
        break;

    case 2:
        console.log(a-b);
        break;

}
```

---

# À retenir

✓ switch simplifie les choix multiples

✓ break est indispensable

✓ default gère les cas non prévus

✓ switch est souvent plus lisible que plusieurs else if

---

# Test de niveau

## QCM

1. Quel mot-clé permet de gérer un cas ?

---

2. Quel mot-clé évite l'exécution des cas suivants ?

---

3. Quel mot-clé gère les valeurs non prévues ?

---

## Défi

Créer un programme qui affiche le jour de la semaine à partir d'un nombre compris entre 1 et 7.
