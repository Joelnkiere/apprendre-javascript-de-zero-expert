# Module 11 : Les Conditions

## Objectifs

À la fin de ce module, vous serez capable de :

- Utiliser if
- Utiliser if...else
- Utiliser else if
- Utiliser l'opérateur ternaire
- Prendre des décisions dans un programme

---

# Pourquoi utiliser des conditions ?

Les conditions permettent à un programme de prendre des décisions.

Exemple :

- Autoriser ou refuser une connexion
- Vérifier l'âge d'un utilisateur
- Calculer une mention

---

# La structure if

Syntaxe :

```javascript
if (condition) {
    // code exécuté si la condition est vraie
}
```

---

# Exemple

```javascript
let age = 20;

if (age >= 18) {
    console.log("Majeur");
}
```

---

# Diagramme logique

```text
Condition ?
   |
Oui ----> Exécuter le bloc
   |
Non ----> Ignorer le bloc
```

---

# if...else

Permet de gérer deux cas.

```javascript
if (condition) {
    // vrai
} else {
    // faux
}
```

---

# Exemple

```javascript
let age = 16;

if (age >= 18) {
    console.log("Majeur");
} else {
    console.log("Mineur");
}
```

---

# else if

Permet de gérer plusieurs possibilités.

```javascript
if (condition1) {

} else if (condition2) {

} else {

}
```

---

# Exemple : Notes

```javascript
let note = 15;

if (note >= 16) {
    console.log("Très Bien");
}
else if (note >= 14) {
    console.log("Bien");
}
else if (note >= 10) {
    console.log("Passable");
}
else {
    console.log("Échec");
}
```

---

# Conditions imbriquées

```javascript
let age = 25;
let permis = true;

if (age >= 18) {

    if (permis) {
        console.log("Peut conduire");
    }

}
```

---

# Cas pratique : Accès à une plateforme

```javascript
let utilisateurActif = true;

if (utilisateurActif) {
    console.log("Accès autorisé");
}
else {
    console.log("Compte désactivé");
}
```

---

# Opérateur ternaire

Version courte de if...else.

Syntaxe :

```javascript
condition
? valeurSiVrai
: valeurSiFaux
```

---

# Exemple

```javascript
let age = 20;

let statut =
    age >= 18
    ? "Majeur"
    : "Mineur";

console.log(statut);
```

---

# Cas pratique : Moyenne

```javascript
let moyenne = 13;

if (moyenne >= 10) {
    console.log("Réussi");
}
else {
    console.log("Échec");
}
```

---

# Projet : Vérification d'âge

```javascript
let age =
    Number(prompt("Entrez votre âge"));

if (age >= 18) {
    alert("Bienvenue");
}
else {
    alert("Accès refusé");
}
```

---

# Exercices

## Exercice 1

Créer un programme qui affiche :

```text
Adulte
```

si l'âge est supérieur ou égal à 18.

---

## Exercice 2

Créer un programme qui affiche :

```text
Positif
```

ou

```text
Négatif
```

selon un nombre.

---

## Exercice 3

Créer un programme qui affiche :

- Excellent
- Bien
- Moyen
- Échec

selon la note.

---

# Corrigés

## Correction Exercice 1

```javascript
let age = 18;

if (age >= 18) {
    console.log("Adulte");
}
```

---

## Correction Exercice 2

```javascript
let nombre = -5;

if (nombre >= 0) {
    console.log("Positif");
}
else {
    console.log("Négatif");
}
```

---

## Correction Exercice 3

```javascript
let note = 15;

if (note >= 16) {
    console.log("Excellent");
}
else if (note >= 14) {
    console.log("Bien");
}
else if (note >= 10) {
    console.log("Moyen");
}
else {
    console.log("Échec");
}
```

---

# À retenir

✓ if exécute du code si une condition est vraie

✓ else gère le cas contraire

✓ else if permet plusieurs choix

✓ Le ternaire simplifie certaines conditions

✓ Les conditions sont essentielles dans tout programme

---

# Test de niveau

## QCM

1. Quel mot-clé permet de gérer le cas contraire ?

a) else

b) switch

c) return

---

2. Quel mot-clé permet plusieurs conditions ?

a) break

b) else if

c) while

---

3. Quelle est la version courte de if...else ?

---

## Défi

Créer un programme qui :

- demande une moyenne
- affiche la mention obtenue
