# Module 9 : Les Opérateurs

## Objectifs

À la fin de ce module, vous serez capable de :

- Utiliser les opérateurs arithmétiques
- Comprendre la priorité des opérations
- Utiliser l'incrémentation
- Utiliser les affectations composées

---

# Introduction

Les opérateurs permettent d'effectuer des calculs.

Exemple :

```javascript
5 + 3
```

---

# Addition

```javascript
let resultat = 5 + 3;
```

Résultat :

```text
8
```

---

# Soustraction

```javascript
let resultat = 10 - 4;
```

Résultat :

```text
6
```

---

# Multiplication

```javascript
let resultat = 5 * 2;
```

Résultat :

```text
10
```

---

# Division

```javascript
let resultat = 20 / 4;
```

Résultat :

```text
5
```

---

# Modulo (%)

Retourne le reste d'une division.

```javascript
10 % 3
```

Résultat :

```text
1
```

---

# Utilité du modulo

Déterminer si un nombre est pair :

```javascript
let nombre = 8;

console.log(nombre % 2);
```

Résultat :

```text
0
```

---

# Exponentiation

```javascript
2 ** 3
```

Résultat :

```text
8
```

---

# Priorité des opérations

```javascript
5 + 2 * 3
```

Résultat :

```text
11
```

---

# Utiliser des parenthèses

```javascript
(5 + 2) * 3
```

Résultat :

```text
21
```

---

# Incrémentation

Augmente de 1.

```javascript
let compteur = 1;

compteur++;
```

---

Equivalent :

```javascript
compteur = compteur + 1;
```

---

# Décrémentation

```javascript
let compteur = 10;

compteur--;
```

---

# Affectation composée

Addition :

```javascript
let total = 10;

total += 5;
```

---

Equivalent :

```javascript
total = total + 5;
```

---

# Autres opérateurs

```javascript
+=
-=
*=
/=
%=
```

---

# Exemple pratique

```javascript
let solde = 100;

solde += 50;
solde -= 20;

console.log(solde);
```

---

# Exercices

## Exercice 1

Calculer :

```text
15 + 20
```

---

## Exercice 2

Calculer :

```text
100 % 7
```

---

## Exercice 3

Créer une variable compteur et l'incrémenter 5 fois.

---

# Corrigés

## Correction Exercice 1

```javascript
let resultat = 15 + 20;
```

---

## Correction Exercice 2

```javascript
let resultat = 100 % 7;
```

---

## Correction Exercice 3

```javascript
let compteur = 0;

compteur++;
compteur++;
compteur++;
compteur++;
compteur++;
```

---

# À retenir

✓ + additionne

✓ - soustrait

✓ * multiplie

✓ / divise

✓ % retourne le reste

✓ ++ incrémente

✓ -- décrémente

✓ += simplifie l'écriture

---

# Test de niveau

## QCM

1. Quel opérateur retourne le reste d'une division ?

a) /

b) %

c) *

---

2. Quel est le résultat ?

```javascript
5 + 3 * 2
```

---

3. Que fait ++ ?

---

## Défi

Créer une calculatrice qui :

- demande deux nombres
- affiche :
  - somme
  - différence
  - produit
  - quotient
