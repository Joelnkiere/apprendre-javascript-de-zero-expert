# Module 18 : Les Fonctions Fléchées (Arrow Functions)

## Objectifs

À la fin de ce module, vous serez capable de :

- Utiliser les Arrow Functions
- Comprendre leur syntaxe
- Simplifier votre code

---

# Introduction

Les Arrow Functions ont été introduites avec ES6.

Elles permettent d'écrire des fonctions plus courtes.

---

# Syntaxe classique

```javascript
function addition(a,b){

    return a+b;

}
```

---

# Arrow Function

```javascript
const addition =
    (a,b) => {

        return a+b;

    };
```

---

# Exemple

```javascript
console.log(
    addition(10,5)
);
```

---

# Retour implicite

Si une seule instruction est retournée :

```javascript
const addition =
    (a,b) => a+b;
```

---

# Paramètre unique

```javascript
const carre =
    n => n*n;
```

---

# Aucun paramètre

```javascript
const bonjour =
    () => {

        console.log("Bonjour");

    };
```

---

# Exemple pratique

```javascript
const calculerTVA =
    prix => prix * 0.16;
```

---

# Exemple avec tableau

```javascript
let notes =
    [10,15,18];

notes.forEach(
    note => console.log(note)
);
```

---

# Comparaison

Fonction classique :

```javascript
function carre(n){

    return n*n;

}
```

---

Arrow :

```javascript
const carre =
    n => n*n;
```

---

# Quand utiliser les Arrow Functions ?

Très souvent :

- React
- Node.js
- Next.js
- Applications modernes

---

# Projet

```javascript
const moyenne =
    (a,b,c) =>
        (a+b+c)/3;

console.log(
    moyenne(10,15,20)
);
```

---

# Exercices

## Exercice 1

Créer une Arrow Function qui affiche votre prénom.

---

## Exercice 2

Créer une Arrow Function qui calcule le périmètre d'un rectangle.

---

## Exercice 3

Créer une Arrow Function qui retourne le cube d'un nombre.

---

# Corrigés

## Correction Exercice 1

```javascript
const afficherPrenom =
    () => console.log("Joel");
```

---

## Correction Exercice 2

```javascript
const perimetre =
    (l,L) =>
        2*(l+L);
```

---

## Correction Exercice 3

```javascript
const cube =
    n => n*n*n;
```

---

# À retenir

✓ Les Arrow Functions simplifient le code

✓ => est la syntaxe principale

✓ Elles sont très utilisées aujourd'hui

✓ Elles permettent un retour implicite

---

# Test de niveau

## QCM

1. Quel symbole caractérise une Arrow Function ?

---

2. Peut-on omettre les parenthèses avec un seul paramètre ?

---

3. Qu'est-ce qu'un retour implicite ?

---

## Défi

Créer une Arrow Function qui calcule :

```text
(prix × quantité)
```

et retourne le montant total.
