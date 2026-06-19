# Module 8 : Conversions de Types

## Objectifs

À la fin de ce module, vous serez capable de :

- Convertir une valeur en nombre
- Convertir une valeur en chaîne de caractères
- Convertir une valeur en booléen
- Comprendre les conversions implicites
- Éviter les pièges courants

---

# Pourquoi convertir les types ?

Dans une application, les données peuvent provenir :

- d'un formulaire
- d'une API
- d'une base de données
- d'une saisie utilisateur

Très souvent, il faut transformer ces données avant de les utiliser.

---

# Exemple

```javascript
let age = prompt("Quel est votre âge ?");
```

Même si l'utilisateur saisit :

```text
25
```

JavaScript reçoit :

```javascript
"25"
```

et non :

```javascript
25
```

---

# Conversion vers Number

Permet de transformer du texte en nombre.

```javascript
Number("25")
```

Résultat :

```javascript
25
```

---

# Exemple

```javascript
let a = "10";
let b = "20";

console.log(Number(a) + Number(b));
```

Résultat :

```text
30
```

---

# Sans conversion

```javascript
let a = "10";
let b = "20";

console.log(a + b);
```

Résultat :

```text
1020
```

---

# parseInt()

Convertit vers un entier.

```javascript
parseInt("15")
```

Résultat :

```text
15
```

---

# Exemple

```javascript
parseInt("15 ans")
```

Résultat :

```text
15
```

---

# parseFloat()

Convertit vers un nombre décimal.

```javascript
parseFloat("19.99")
```

Résultat :

```text
19.99
```

---

# Conversion vers String

Permet de transformer une valeur en texte.

```javascript
String(50)
```

Résultat :

```text
"50"
```

---

# Exemple

```javascript
let age = 25;

console.log(String(age));
```

---

# Conversion vers Boolean

Permet d'obtenir :

```javascript
true
```

ou

```javascript
false
```

---

# Valeurs considérées comme false

```javascript
false
0
""
null
undefined
NaN
```

---

# Exemple

```javascript
Boolean(0)
```

Résultat :

```javascript
false
```

---

```javascript
Boolean(100)
```

Résultat :

```javascript
true
```

---

# Conversion implicite

JavaScript effectue parfois des conversions automatiquement.

---

# Exemple

```javascript
console.log("5" * 2);
```

Résultat :

```text
10
```

---

# Pourquoi ?

JavaScript convertit automatiquement :

```javascript
"5"
```

en

```javascript
5
```

---

# Autre exemple

```javascript
console.log("5" + 2);
```

Résultat :

```text
52
```

---

# Piège fréquent

```javascript
console.log("10" - 2);
```

Résultat :

```text
8
```

---

```javascript
console.log("10" + 2);
```

Résultat :

```text
102
```

---

# Bonnes pratiques

✓ Convertir explicitement

✓ Éviter de compter sur les conversions automatiques

✓ Utiliser Number() lorsque possible

---

# Exercices

## Exercice 1

Convertir :

```javascript
"150"
```

en nombre.

---

## Exercice 2

Convertir :

```javascript
500
```

en texte.

---

## Exercice 3

Créer une mini calculatrice qui additionne deux valeurs saisies avec prompt().

---

# Corrigés

## Correction Exercice 1

```javascript
let valeur = Number("150");
```

---

## Correction Exercice 2

```javascript
let valeur = String(500);
```

---

## Correction Exercice 3

```javascript
let a = prompt("Nombre 1");
let b = prompt("Nombre 2");

let resultat =
    Number(a) +
    Number(b);

alert(resultat);
```

---

# À retenir

✓ Number() convertit en nombre

✓ String() convertit en texte

✓ Boolean() convertit en booléen

✓ JavaScript effectue parfois des conversions automatiques

✓ Toujours privilégier les conversions explicites

---

# Test de niveau

## QCM

1. Quelle fonction convertit une chaîne en nombre ?

a) String()

b) Number()

c) Boolean()

---

2. Quel résultat obtient-on ?

```javascript
"10" + 5
```

---

3. Quel résultat obtient-on ?

```javascript
Boolean(0)
```

---

## Défi

Créer un programme qui :

- demande deux nombres
- calcule leur somme
- affiche le résultat
