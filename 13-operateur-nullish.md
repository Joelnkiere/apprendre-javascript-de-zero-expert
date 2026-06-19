# Module 13 : L'Opérateur Nullish (??)

## Objectifs

À la fin de ce module, vous serez capable de :

- Comprendre ??
- Le comparer à ||
- Gérer les valeurs nulles ou undefined

---

# Le problème

Parfois une valeur n'existe pas.

Exemple :

```javascript
let nomUtilisateur;
```

---

# Solution classique

```javascript
let nom =
    nomUtilisateur || "Invité";
```

---

# Résultat

```text
Invité
```

---

# Limite de ||

```javascript
let score = 0;

let resultat =
    score || 100;
```

Résultat :

```text
100
```

---

# Pourquoi est-ce un problème ?

Parce que :

```javascript
0
```

est une valeur valide.

---

# L'opérateur ??

Syntaxe :

```javascript
valeur ?? valeurParDefaut
```

---

# Exemple

```javascript
let score = 0;

let resultat =
    score ?? 100;

console.log(resultat);
```

Résultat :

```text
0
```

---

# Fonctionnement

?? remplace uniquement :

```javascript
null
```

ou

```javascript
undefined
```

---

# Exemple

```javascript
let nom;

console.log(
    nom ?? "Invité"
);
```

Résultat :

```text
Invité
```

---

# Cas pratique API

```javascript
let utilisateur = {
    nom: null
};

console.log(
    utilisateur.nom ?? "Inconnu"
);
```

---

# Comparaison

```javascript
0 || 100
```

Résultat :

```text
100
```

---

```javascript
0 ?? 100
```

Résultat :

```text
0
```

---

# Projet

```javascript
let nom =
    prompt("Nom");

console.log(
    nom ?? "Invité"
);
```

---

# Exercices

## Exercice 1

Afficher "Utilisateur" si une variable est undefined.

---

## Exercice 2

Tester la différence entre :

```javascript
||
```

et

```javascript
??
```

avec la valeur :

```javascript
0
```

---

# Corrigés

## Correction Exercice 1

```javascript
let nom;

console.log(
    nom ?? "Utilisateur"
);
```

---

## Correction Exercice 2

```javascript
console.log(0 || 50);
console.log(0 ?? 50);
```

---

# À retenir

✓ ?? ne remplace que null ou undefined

✓ || remplace plusieurs valeurs falsy

✓ ?? est souvent plus sûr

---

# Test de niveau

## QCM

1. Que remplace l'opérateur ?? ?

---

2. Quelle différence existe entre || et ?? ?

---

## Défi

Créer un système qui affiche :

- le nom saisi
- sinon "Invité"
