# Module 17 : Function Expressions

## Objectifs

À la fin de ce module, vous serez capable de :

- Comprendre les Function Expressions
- Les comparer aux fonctions déclarées
- Choisir la bonne approche

---

# Déclaration classique

```javascript
function addition(a,b){

    return a+b;

}
```

---

# Function Expression

Une fonction peut être stockée dans une variable.

```javascript
const addition =
    function(a,b){

        return a+b;

    };
```

---

# Utilisation

```javascript
console.log(
    addition(5,3)
);
```

---

# Pourquoi utiliser cette approche ?

Parce qu'une fonction est aussi une valeur.

Comme :

```javascript
let nom = "Joel";
```

On peut écrire :

```javascript
let calcul =
    function(){};
```

---

# Comparaison

Fonction déclarée :

```javascript
function bonjour(){

}
```

---

Expression :

```javascript
const bonjour =
    function(){

    };
```

---

# Hoisting

Les fonctions déclarées sont accessibles avant leur définition.

---

# Exemple

```javascript
saluer();

function saluer(){

    console.log("Bonjour");

}
```

Fonctionne.

---

# Function Expression

```javascript
saluer();

const saluer =
    function(){

    };
```

Erreur.

---

# Exemple pratique

```javascript
const calculerMoyenne =
    function(a,b,c){

        return (a+b+c)/3;

    };

console.log(
    calculerMoyenne(10,12,18)
);
```

---

# Projet

Gestion d'étudiants.

```javascript
const afficherEtudiant =
    function(nom){

        console.log(
            "Étudiant : " + nom
        );

    };

afficherEtudiant("Joel");
```

---

# Exercices

## Exercice 1

Créer une Function Expression qui affiche votre nom.

---

## Exercice 2

Créer une Function Expression qui multiplie deux nombres.

---

## Exercice 3

Créer une Function Expression qui retourne le carré d'un nombre.

---

# Corrigés

## Correction Exercice 1

```javascript
const afficherNom =
    function(){

        console.log("Joel");

    };
```

---

## Correction Exercice 2

```javascript
const multiplier =
    function(a,b){

        return a*b;

    };
```

---

## Correction Exercice 3

```javascript
const carre =
    function(n){

        return n*n;

    };
```

---

# À retenir

✓ Une Function Expression est stockée dans une variable

✓ Elle peut être passée comme valeur

✓ Elle n'est pas hoistée comme une fonction classique

✓ Très utilisée dans les applications modernes

---

# Test de niveau

## QCM

1. Où est stockée une Function Expression ?

---

2. Peut-on appeler une Function Expression avant sa déclaration ?

---

3. Quelle différence majeure existe avec une fonction classique ?

---

## Défi

Créer une Function Expression qui calcule la moyenne de quatre notes.
