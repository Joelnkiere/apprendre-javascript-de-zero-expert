# Module 5 : Variables

## Objectifs

- Comprendre le stockage des données
- Utiliser let
- Utiliser const
- Respecter les conventions

---

# Qu'est-ce qu'une variable ?

Une variable est une zone mémoire qui stocke une valeur.

Exemple :

```javascript
let nom = "Joel";
```

---

# Représentation

```text
nom
↓
Joel
```

---

# Déclaration avec let

```javascript
let age = 25;
```

Affichage :

```javascript
console.log(age);
```

Résultat :

```text
25
```

---

# Modification

```javascript
let age = 25;

age = 30;

console.log(age);
```

Résultat :

```text
30
```

---

# Déclaration avec const

```javascript
const pays = "RDC";
```

---

# Tentative de modification

```javascript
const pays = "RDC";

pays = "France";
```

Erreur :

```text
TypeError
```

---

# Différence entre let et const

let :

```javascript
let age = 25;
age = 30;
```

Possible.

const :

```javascript
const age = 25;
age = 30;
```

Impossible.

---

# Convention camelCase

Correct :

```javascript
let nomComplet;
let dateNaissance;
let montantTotal;
```

Incorrect :

```javascript
let nom_complet;
let NOM;
let a;
```

---

# Exemple professionnel

```javascript
const tauxTVA = 16;

let prixProduit = 100;

let prixFinal =
    prixProduit +
    (prixProduit * tauxTVA / 100);

console.log(prixFinal);
```

---

# Exercice 1

Créer une variable :

```javascript
prenom
```

ayant pour valeur votre prénom.

---

# Correction

```javascript
let prenom = "Joel";
```

---

# Exercice 2

Créer :

```javascript
const pays = "RDC";
```

puis essayer de modifier sa valeur.

Que se passe-t-il ?

---

# Correction

Une erreur apparaît.

---

# Exercice 3

Calculer :

```text
10 + 15
```

à l'aide de variables.

---

# Correction

```javascript
let a = 10;
let b = 15;

let resultat = a + b;

console.log(resultat);
```

---

# À retenir

✓ Une variable stocke une valeur

✓ let permet la modification

✓ const protège la valeur

✓ Utiliser camelCase

✓ Donner des noms explicites

---

# Test de niveau

1. Quelle déclaration permet la modification ?

a) const
b) let

Réponse : b

---

2. Une constante peut-elle être modifiée ?

Réponse : Non

---

3. Corriger :

```javascript
let Nom Complet;
```

Réponse :

```javascript
let nomComplet;
```
