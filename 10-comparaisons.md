# Module 10 : Les Comparaisons

## Objectifs

À la fin de ce module, vous serez capable de :

- Comparer des valeurs
- Comprendre == et ===
- Comprendre != et !==
- Construire des conditions fiables

---

# Pourquoi comparer ?

Les comparaisons servent à prendre des décisions.

Exemple :

```javascript
age >= 18
```

---

# Égalité

```javascript
5 == 5
```

Résultat :

```javascript
true
```

---

# Différence

```javascript
5 != 3
```

Résultat :

```javascript
true
```

---

# Supérieur

```javascript
10 > 5
```

---

# Inférieur

```javascript
2 < 8
```

---

# Supérieur ou égal

```javascript
10 >= 10
```

---

# Inférieur ou égal

```javascript
5 <= 5
```

---

# Double égal (==)

Compare les valeurs.

```javascript
"5" == 5
```

Résultat :

```javascript
true
```

---

# Pourquoi ?

JavaScript convertit automatiquement les types.

---

# Triple égal (===)

Compare :

- la valeur
- le type

---

```javascript
"5" === 5
```

Résultat :

```javascript
false
```

---

# Recommandation

Toujours privilégier :

```javascript
===
```

---

# Différence stricte

```javascript
!== 
```

---

Exemple :

```javascript
"10" !== 10
```

Résultat :

```javascript
true
```

---

# Cas pratique

```javascript
let motDePasse = "1234";

console.log(motDePasse === "1234");
```

---

# Exercices

## Exercice 1

Comparer :

```javascript
15 === 15
```

---

## Exercice 2

Comparer :

```javascript
"25" === 25
```

---

## Exercice 3

Créer une variable age et vérifier si elle est supérieure ou égale à 18.

---

# Corrigés

## Correction Exercice 1

```javascript
console.log(15 === 15);
```

---

## Correction Exercice 2

```javascript
console.log("25" === 25);
```

---

## Correction Exercice 3

```javascript
let age = 20;

console.log(age >= 18);
```

---

# À retenir

✓ == compare les valeurs

✓ === compare les valeurs et les types

✓ !== compare strictement les différences

✓ Toujours préférer ===

---

# Test de niveau

## QCM

1. Quelle comparaison est recommandée ?

a) ==

b) ===

---

2. Quelle différence existe entre == et === ?

---

3. Quel est le résultat ?

```javascript
"10" === 10
```

---

## Défi

Créer un programme qui vérifie :

- si un utilisateur est majeur
- si un mot de passe est correct
