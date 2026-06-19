# Module 3 : Structure du Code

## Objectifs

- Écrire un code lisible
- Utiliser les commentaires
- Comprendre l'indentation
- Respecter les conventions

---

# Pourquoi structurer son code ?

Un code bien structuré :

- est plus facile à lire
- réduit les erreurs
- facilite la maintenance

---

# Commentaire simple

```javascript
// Ceci est un commentaire
```

Exemple :

```javascript
// Affichage du prénom
console.log("Joel");
```

---

# Commentaire multiligne

```javascript
/*
Commentaire
sur
plusieurs lignes
*/
```

---

# Quand utiliser les commentaires ?

Pour expliquer :

- une logique complexe
- une formule
- une décision métier

Éviter :

```javascript
// afficher prénom
console.log("Joel");
```

Le code est déjà évident.

---

# Indentation

Mauvais exemple :

```javascript
if(age > 18){
console.log("Majeur");
}
```

Bon exemple :

```javascript
if(age > 18){
    console.log("Majeur");
}
```

---

# Points-virgules

JavaScript les ajoute automatiquement.

Exemple :

```javascript
let age = 20
console.log(age)
```

Mais recommandé :

```javascript
let age = 20;
console.log(age);
```

---

# Formatage professionnel

```javascript
function calculerMoyenne(note1, note2) {
    return (note1 + note2) / 2;
}
```

---

# Exercice

Corriger :

```javascript
if(age>=18){
console.log("ok")
}
```

---

# Correction

```javascript
if(age >= 18){
    console.log("ok");
}
```

---

# À retenir

✓ Utiliser l'indentation

✓ Utiliser des commentaires utiles

✓ Garder un format cohérent

✓ Les points-virgules sont recommandés

---

# Test de niveau

1. Quel symbole démarre un commentaire simple ?

Réponse :

```javascript
//
```

2. Quel symbole démarre un commentaire multiligne ?

Réponse :

```javascript
/*
```

3. Pourquoi indenter le code ?

Réponse :

Pour améliorer la lisibilité.
