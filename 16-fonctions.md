# Module 16 : Les Fonctions

## Objectifs

À la fin de ce module, vous serez capable de :

- Comprendre l'utilité des fonctions
- Déclarer une fonction
- Utiliser des paramètres
- Retourner une valeur
- Comprendre la portée (Scope)

---

# Pourquoi utiliser des fonctions ?

Une fonction permet de regrouper des instructions réutilisables.

Sans fonction :

```javascript
console.log("Bonjour Joel");
console.log("Bonjour Sarah");
console.log("Bonjour David");
```

---

Avec fonction :

```javascript
function saluer(nom){
    console.log("Bonjour " + nom);
}

saluer("Joel");
saluer("Sarah");
saluer("David");
```

---

# Déclaration d'une fonction

Syntaxe :

```javascript
function nomFonction(){

}
```

---

# Exemple simple

```javascript
function direBonjour(){

    console.log("Bonjour");

}
```

---

# Appel d'une fonction

```javascript
direBonjour();
```

---

# Paramètres

Les paramètres permettent de recevoir des données.

```javascript
function saluer(nom){

    console.log("Bonjour " + nom);

}
```

---

# Exemple

```javascript
saluer("Joel");
```

Résultat :

```text
Bonjour Joel
```

---

# Plusieurs paramètres

```javascript
function addition(a, b){

    console.log(a + b);

}
```

---

# Exemple

```javascript
addition(10, 20);
```

Résultat :

```text
30
```

---

# Valeur de retour

Une fonction peut retourner un résultat.

---

# Exemple

```javascript
function addition(a, b){

    return a + b;

}
```

---

# Utilisation du résultat

```javascript
let resultat =
    addition(10, 20);

console.log(resultat);
```

---

# Pourquoi return ?

Permet :

- de récupérer une valeur
- de réutiliser le résultat
- d'effectuer des calculs complexes

---

# Exemple professionnel

```javascript
function calculerTVA(prix){

    return prix * 0.16;

}

let tva =
    calculerTVA(100);

console.log(tva);
```

---

# Scope (Portée)

Les variables déclarées dans une fonction restent dans la fonction.

---

# Exemple

```javascript
function test(){

    let message =
        "Bonjour";

}

console.log(message);
```

Erreur :

```text
message is not defined
```

---

# Scope local

```javascript
function test(){

    let age = 20;

    console.log(age);

}
```

---

# Scope global

```javascript
let pays = "RDC";

function afficher(){

    console.log(pays);

}
```

---

# Projet : Calculatrice

```javascript
function addition(a,b){
    return a+b;
}

function soustraction(a,b){
    return a-b;
}

function multiplication(a,b){
    return a*b;
}

function division(a,b){
    return a/b;
}

console.log(addition(10,5));
```

---

# Exercices

## Exercice 1

Créer une fonction qui affiche :

```text
Bienvenue
```

---

## Exercice 2

Créer une fonction qui additionne deux nombres.

---

## Exercice 3

Créer une fonction qui calcule l'aire d'un rectangle.

Formule :

```text
longueur × largeur
```

---

# Corrigés

## Correction Exercice 1

```javascript
function bienvenue(){

    console.log("Bienvenue");

}
```

---

## Correction Exercice 2

```javascript
function addition(a,b){

    return a+b;

}
```

---

## Correction Exercice 3

```javascript
function aireRectangle(
    longueur,
    largeur
){

    return longueur * largeur;

}
```

---

# À retenir

✓ Une fonction évite la répétition

✓ Les paramètres reçoivent des données

✓ return renvoie un résultat

✓ Le scope protège les variables locales

✓ Les fonctions sont indispensables en programmation

---

# Test de niveau

## QCM

1. Quel mot-clé permet de créer une fonction ?

---

2. Quel mot-clé renvoie une valeur ?

---

3. Qu'est-ce qu'un paramètre ?

---

## Défi

Créer une fonction qui :

- reçoit trois notes
- calcule leur moyenne
- retourne le résultat
