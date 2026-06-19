# Module 7 : Interaction Utilisateur

## Objectifs

À la fin de ce module vous serez capable de :

- Afficher des messages
- Demander des informations à l'utilisateur
- Obtenir une confirmation
- Réaliser un mini projet interactif

---

# Pourquoi interagir avec l'utilisateur ?

Une application utile doit pouvoir :

- afficher des informations
- recevoir des données
- obtenir des confirmations

---

# alert()

Permet d'afficher un message.

```javascript
alert("Bienvenue dans la formation JavaScript");
```

---

# Fonctionnement

Lorsque alert apparaît :

- l'utilisateur doit cliquer sur OK
- le programme attend

---

# Exemple pratique

```javascript
alert("Votre inscription est réussie");
```

---

# prompt()

Permet de demander une information.

```javascript
prompt("Quel est votre nom ?");
```

---

# Stocker la réponse

```javascript
let nom = prompt("Quel est votre nom ?");

console.log(nom);
```

---

# Exemple complet

```javascript
let prenom = prompt("Entrez votre prénom");

alert("Bonjour " + prenom);
```

---

# confirm()

Permet d'obtenir une réponse Oui/Non.

```javascript
confirm("Voulez-vous continuer ?");
```

---

# Valeur retournée

Si l'utilisateur clique OK :

```javascript
true
```

Si l'utilisateur clique Annuler :

```javascript
false
```

---

# Exemple

```javascript
let continuer = confirm("Voulez-vous quitter ?");

console.log(continuer);
```

---

# Cas pratique

```javascript
let majeur = confirm("Avez-vous plus de 18 ans ?");

if (majeur) {
    alert("Accès autorisé");
}
```

---

# Mini Projet : Calculatrice

Étape 1

```javascript
let nombre1 = prompt("Entrez le premier nombre");
```

---

Étape 2

```javascript
let nombre2 = prompt("Entrez le deuxième nombre");
```

---

Étape 3

```javascript
let resultat =
    Number(nombre1) +
    Number(nombre2);
```

---

Étape 4

```javascript
alert("Résultat : " + resultat);
```

---

# Version complète

```javascript
let nombre1 = prompt("Premier nombre");
let nombre2 = prompt("Deuxième nombre");

let resultat =
    Number(nombre1) +
    Number(nombre2);

alert("Résultat : " + resultat);
```

---

# Exercice 1

Demander le prénom d'un utilisateur puis afficher :

```text
Bonjour PRENOM
```

---

# Exercice 2

Demander :

```text
Quel est votre âge ?
```

Puis afficher :

```text
Vous avez XX ans
```

---

# Exercice 3

Créer un programme qui demande deux nombres et affiche leur multiplication.

---

# Corrigés

## Correction Exercice 1

```javascript
let prenom = prompt("Votre prénom ?");

alert("Bonjour " + prenom);
```

---

## Correction Exercice 2

```javascript
let age = prompt("Quel est votre âge ?");

alert("Vous avez " + age + " ans");
```

---

## Correction Exercice 3

```javascript
let a = prompt("Nombre 1");
let b = prompt("Nombre 2");

let resultat =
    Number(a) * Number(b);

alert(resultat);
```

---

# À retenir

✓ alert() affiche un message

✓ prompt() demande une information

✓ confirm() retourne true ou false

✓ Les valeurs saisies sont souvent des chaînes de caractères

✓ Number() permet de convertir en nombre

---

# Test de niveau

## QCM

1. Quelle fonction permet de demander une information ?

a) alert()

b) prompt()

c) confirm()

---

2. Quelle fonction retourne true ou false ?

a) alert()

b) prompt()

c) confirm()

---

3. Quel est le résultat de prompt() ?

a) Un nombre

b) Une chaîne de caractères

c) Un objet

---

## Défi pratique

Créer un programme qui :

1. Demande le prénom
2. Demande l'âge
3. Affiche un message personnalisé contenant les deux informations
