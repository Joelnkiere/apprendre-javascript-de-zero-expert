# Module 19 : JavaScript Specials

## Objectifs

À la fin de ce module, vous serez capable de :

- Identifier les erreurs fréquentes des débutants
- Adopter les bonnes pratiques professionnelles
- Écrire un code plus propre
- Préparer la suite de votre apprentissage JavaScript

---

# Les erreurs les plus fréquentes

Même les développeurs expérimentés font des erreurs.

L'objectif n'est pas d'éviter toutes les erreurs.

L'objectif est de savoir les identifier rapidement.

---

# Erreur 1 : Oublier de déclarer une variable

Mauvais exemple :

```javascript
nom = "Joel";
```

---

Correct :

```javascript
let nom = "Joel";
```

---

# Erreur 2 : Confondre = et ===

Mauvais exemple :

```javascript
if(age = 18){

}
```

---

Correct :

```javascript
if(age === 18){

}
```

---

# Erreur 3 : Oublier les accolades

Mauvais exemple :

```javascript
if(age >= 18)
    console.log("Majeur");
    console.log("Accès autorisé");
```

---

Correct :

```javascript
if(age >= 18){
    console.log("Majeur");
    console.log("Accès autorisé");
}
```

---

# Erreur 4 : Mauvaise comparaison de type

Mauvais exemple :

```javascript
let age = prompt("Age");

if(age === 18){

}
```

---

Pourquoi ?

prompt retourne une chaîne de caractères.

---

Correct :

```javascript
let age =
    Number(prompt("Age"));

if(age === 18){

}
```

---

# Erreur 5 : Boucle infinie

Mauvais exemple :

```javascript
let i = 1;

while(i <= 10){

    console.log(i);

}
```

---

Pourquoi ?

La variable i n'est jamais modifiée.

---

Correct :

```javascript
let i = 1;

while(i <= 10){

    console.log(i);

    i++;

}
```

---

# Erreur 6 : Oublier return

Mauvais exemple :

```javascript
function addition(a,b){

    a+b;

}
```

---

Correct :

```javascript
function addition(a,b){

    return a+b;

}
```

---

# Bonnes pratiques professionnelles

---

# Utiliser des noms explicites

Mauvais :

```javascript
let x = 10;
let y = 20;
```

---

Bon :

```javascript
let prixProduit = 10;
let quantiteProduit = 20;
```

---

# Une seule responsabilité

Mauvais :

```javascript
function gestionComplete(){

}
```

---

Bon :

```javascript
function calculerTotal(){

}

function afficherFacture(){

}
```

---

# Commenter intelligemment

Mauvais :

```javascript
// ajouter deux nombres
let total = a+b;
```

---

Bon :

```javascript
// TVA appliquée selon la législation
let total = prix + taxe;
```

---

# Utiliser const par défaut

Préférer :

```javascript
const tauxTVA = 16;
```

---

Utiliser let seulement lorsque la valeur change.

---

# Organiser son code

Ordre conseillé :

1. Constantes
2. Variables
3. Fonctions
4. Programme principal

---

# Exemple professionnel

```javascript
const TVA = 16;

function calculerTVA(prix){

    return prix * TVA / 100;

}

let prixProduit = 100;

let montantTVA =
    calculerTVA(prixProduit);

console.log(montantTVA);
```

---

# Conseils professionnels

---

# Lire du code

Chaque semaine :

- GitHub
- Open Source
- Tutoriels

---

# Programmer tous les jours

Même :

15 minutes

par jour.

---

# Créer des projets

Exemples :

- Calculatrice
- Gestion des notes
- Todo List
- Convertisseur de devises

---

# Utiliser Git

À apprendre rapidement.

Commandes importantes :

```bash
git init
git add .
git commit
```

---

# Utiliser la documentation

Réflexe professionnel :

MDN

Avant :

- Google
- YouTube
- Forums

---

# Projet pratique

Créer un système qui :

- demande un prix
- demande une quantité
- calcule le total
- affiche le résultat

---

# Exercices

## Exercice 1

Corriger :

```javascript
if(age = 18){
}
```

---

## Exercice 2

Corriger :

```javascript
function somme(a,b){

}
```

pour retourner le résultat.

---

## Exercice 3

Corriger :

```javascript
let i = 1;

while(i <= 5){

    console.log(i);

}
```

---

# Corrigés

## Correction Exercice 1

```javascript
if(age === 18){

}
```

---

## Correction Exercice 2

```javascript
function somme(a,b){

    return a+b;

}
```

---

## Correction Exercice 3

```javascript
let i = 1;

while(i <= 5){

    console.log(i);

    i++;

}
```

---

# À retenir

✓ Déclarer ses variables

✓ Utiliser ===

✓ Éviter les boucles infinies

✓ Utiliser return

✓ Nommer correctement ses variables

✓ Lire la documentation

✓ Créer des projets régulièrement

---

# Test de niveau

## QCM

1. Pourquoi utiliser des noms explicites ?

---

2. Pourquoi utiliser const lorsque c'est possible ?

---

3. Quel est l'intérêt de return ?

---

## Défi

Créer un programme qui :

- demande un prix
- demande une quantité
- calcule le montant total
- affiche le résultat
