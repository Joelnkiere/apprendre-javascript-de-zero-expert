# Module 12 : Les Opérateurs Logiques

## Objectifs

À la fin de ce module, vous serez capable de :

- Utiliser &&
- Utiliser ||
- Utiliser !
- Combiner plusieurs conditions

---

# Pourquoi les opérateurs logiques ?

Ils permettent de combiner plusieurs tests.

Exemple :

Un utilisateur doit :

- être majeur
- avoir un compte actif

---

# Opérateur ET (&&)

Toutes les conditions doivent être vraies.

```javascript
condition1 && condition2
```

---

# Exemple

```javascript
let age = 20;
let permis = true;

console.log(age >= 18 && permis);
```

Résultat :

```javascript
true
```

---

# Tableau simplifié

```text
Vrai && Vrai   => Vrai
Vrai && Faux   => Faux
Faux && Vrai   => Faux
Faux && Faux   => Faux
```

---

# Cas pratique

```javascript
let age = 25;
let abonnement = true;

if (age >= 18 && abonnement) {
    console.log("Accès autorisé");
}
```

---

# Opérateur OU (||)

Une seule condition vraie suffit.

```javascript
condition1 || condition2
```

---

# Exemple

```javascript
let carteVIP = false;
let invitation = true;

console.log(carteVIP || invitation);
```

Résultat :

```javascript
true
```

---

# Tableau simplifié

```text
Vrai || Vrai => Vrai
Vrai || Faux => Vrai
Faux || Vrai => Vrai
Faux || Faux => Faux
```

---

# Cas pratique

```javascript
if (carteVIP || invitation) {
    console.log("Entrée autorisée");
}
```

---

# Opérateur NON (!)

Inverse une valeur.

---

# Exemple

```javascript
let connecte = true;

console.log(!connecte);
```

Résultat :

```javascript
false
```

---

# Exemple pratique

```javascript
let connecte = false;

if (!connecte) {
    console.log("Veuillez vous connecter");
}
```

---

# Combinaison complexe

```javascript
let age = 22;
let abonnement = true;
let suspendu = false;

if (
    age >= 18 &&
    abonnement &&
    !suspendu
) {
    console.log("Accès accordé");
}
```

---

# Projet : Connexion utilisateur

```javascript
let email =
    prompt("Email");

let motDePasse =
    prompt("Mot de passe");

if (
    email === "admin@test.com" &&
    motDePasse === "1234"
) {
    alert("Connexion réussie");
}
else {
    alert("Identifiants incorrects");
}
```

---

# Exercices

## Exercice 1

Vérifier si un utilisateur est :

- majeur
- titulaire d'un permis

---

## Exercice 2

Autoriser l'accès avec :

- carte étudiant
OU
- carte professionnelle

---

## Exercice 3

Afficher un message si l'utilisateur n'est pas connecté.

---

# Corrigés

## Correction Exercice 1

```javascript
if (age >= 18 && permis) {
    console.log("Autorisé");
}
```

---

## Correction Exercice 2

```javascript
if (
    carteEtudiant ||
    carteProfessionnelle
) {
    console.log("Accès");
}
```

---

## Correction Exercice 3

```javascript
if (!connecte) {
    console.log("Connexion requise");
}
```

---

# À retenir

✓ && signifie ET

✓ || signifie OU

✓ ! signifie NON

✓ Les opérateurs logiques permettent de construire des règles complexes

---

# Test de niveau

## QCM

1. Quel opérateur représente ET ?

---

2. Quel opérateur représente OU ?

---

3. Quel opérateur inverse une valeur ?

---

## Défi

Créer un programme qui autorise un étudiant à accéder à une bibliothèque s'il :

- est inscrit
- possède une carte valide
