# Module 6 : Les Types de Données

## Objectifs

À la fin de ce module, vous serez capable de :

- Comprendre les différents types de données
- Identifier le type d'une variable
- Utiliser correctement les types primitifs
- Utiliser typeof

---

# Introduction

Chaque donnée manipulée en JavaScript possède un type.

Exemples :

- Nombre
- Texte
- Vrai/Faux
- Objet

---

# Pourquoi les types sont-ils importants ?

Les types permettent à JavaScript de savoir :

- comment stocker les données
- comment les manipuler
- quelles opérations sont autorisées

---

# Le type Number

Représente les nombres.

Exemples :

```javascript
let age = 25;
let prix = 199.99;
let temperature = -10;
```

---

# Opérations sur les nombres

```javascript
let a = 10;
let b = 5;

console.log(a + b);
console.log(a - b);
console.log(a * b);
console.log(a / b);
```

---

# Le type String

Représente du texte.

```javascript
let nom = "Joel";
let ville = 'Kinshasa';
```

---

# Concaténation

```javascript
let prenom = "Joel";
let nom = "Nkiere";

console.log(prenom + " " + nom);
```

Résultat :

```text
Joel Nkiere
```

---

# Template Literals

```javascript
let prenom = "Joel";

console.log(`Bonjour ${prenom}`);
```

---

# Le type Boolean

Deux valeurs possibles :

```javascript
true
false
```

Exemple :

```javascript
let estConnecte = true;
let estMajeur = false;
```

---

# Cas pratique

```javascript
let age = 20;

console.log(age >= 18);
```

Résultat :

```text
true
```

---

# Undefined

Valeur par défaut d'une variable non initialisée.

```javascript
let nom;

console.log(nom);
```

Résultat :

```text
undefined
```

---

# Null

Représente une absence volontaire de valeur.

```javascript
let utilisateur = null;
```

---

# Différence entre Undefined et Null

Undefined :

```javascript
let x;
```

La valeur n'a jamais été définie.

Null :

```javascript
let x = null;
```

La valeur a été volontairement vidée.

---

# Object

Permet de stocker plusieurs informations.

```javascript
let utilisateur = {
    nom: "Joel",
    age: 25,
    ville: "Kinshasa"
};
```

---

# Accès aux propriétés

```javascript
console.log(utilisateur.nom);
console.log(utilisateur.age);
```

---

# Symbol

Type unique utilisé principalement pour les identifiants.

```javascript
let id = Symbol("id");
```

---

# BigInt

Pour les très grands nombres.

```javascript
let nombre = 123456789123456789123456789n;
```

---

# typeof

Permet de connaître le type.

```javascript
let age = 25;

console.log(typeof age);
```

Résultat :

```text
number
```

---

# Exemples

```javascript
console.log(typeof "Bonjour");
console.log(typeof true);
console.log(typeof null);
console.log(typeof undefined);
```

---

# Exercices

## Exercice 1

Créer :

```javascript
nom
age
ville
```

Puis afficher leurs valeurs.

---

## Exercice 2

Créer un objet représentant un étudiant.

Propriétés :

- nom
- age
- promotion

---

## Exercice 3

Afficher le type des variables suivantes :

```javascript
let a = 50;
let b = "JavaScript";
let c = true;
```

---

# Corrigés

## Correction Exercice 1

```javascript
let nom = "Joel";
let age = 25;
let ville = "Kinshasa";

console.log(nom);
console.log(age);
console.log(ville);
```

---

## Correction Exercice 2

```javascript
let etudiant = {
    nom: "Joel",
    age: 25,
    promotion: "L3"
};
```

---

## Correction Exercice 3

```javascript
console.log(typeof a);
console.log(typeof b);
console.log(typeof c);
```

---

# À retenir

✓ Number représente les nombres

✓ String représente le texte

✓ Boolean représente vrai ou faux

✓ Undefined signifie non défini

✓ Null signifie absence volontaire de valeur

✓ Object stocke plusieurs propriétés

✓ typeof permet d'identifier un type

---

# Test de niveau

## QCM

1. Quel type représente du texte ?

a) Number

b) String

c) Boolean

---

2. Quelle valeur représente l'absence volontaire d'information ?

a) Undefined

b) Null

c) False

---

3. Quel mot-clé permet de connaître le type d'une variable ?

a) type

b) typeof

c) getType

---

## Exercice pratique

Créer une variable pour :

- votre prénom
- votre âge
- votre pays

Puis afficher le type de chacune.
