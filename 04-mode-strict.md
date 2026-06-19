# Module 4 : Mode Strict

## Objectifs

- Comprendre use strict
- Identifier les erreurs évitées
- Adopter les bonnes pratiques

---

# Introduction

Le mode strict permet de rendre JavaScript plus rigoureux.

Activation :

```javascript
"use strict";
```

---

# Pourquoi utiliser use strict ?

Il :

- évite certaines erreurs
- améliore la sécurité
- facilite le débogage

---

# Exemple sans use strict

```javascript
nom = "Joel";

console.log(nom);
```

Le code fonctionne.

Pourtant la variable n'a jamais été déclarée.

---

# Exemple avec use strict

```javascript
"use strict";

nom = "Joel";
```

Erreur :

```text
ReferenceError
```

---

# Déclaration correcte

```javascript
"use strict";

let nom = "Joel";

console.log(nom);
```

---

# Avantages

✓ Réduit les bugs

✓ Code plus propre

✓ Comportement prévisible

---

# Exercice

Trouver l'erreur :

```javascript
"use strict";

age = 25;
```

---

# Correction

```javascript
"use strict";

let age = 25;
```

---

# À retenir

✓ Toujours placer use strict en haut du fichier

✓ Déclarer toutes les variables

✓ Facilite le développement professionnel

---

# Test de niveau

1. Où placer use strict ?

Réponse :

Au début du fichier.

2. Quel est son rôle principal ?

Réponse :

Détecter davantage d'erreurs.
