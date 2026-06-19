# Module 2 : Hello World

## Objectifs

À la fin de ce module, vous serez capable de :

- Exécuter votre premier programme JavaScript
- Comprendre les différentes façons d'intégrer JavaScript
- Appliquer les bonnes pratiques de base

---

# Pourquoi commencer par Hello World ?

Traditionnellement, le premier programme dans un langage consiste à afficher :

"Hello World"

Cela permet de vérifier que tout fonctionne correctement.

---

# Premier programme

```javascript
console.log("Hello World");
```

Explication :

- console : objet fourni par le navigateur
- log() : méthode d'affichage
- "Hello World" : texte affiché

Résultat :

```text
Hello World
```

---

# Script interne

JavaScript directement dans le fichier HTML.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Mon premier programme</title>
</head>
<body>

<script>
    console.log("Bonjour");
</script>

</body>
</html>
```

---

# Comment fonctionne ce code ?

Le navigateur lit :

1. Le HTML
2. Le bloc script
3. Exécute le JavaScript

---

# Script externe

index.html

```html
<script src="app.js"></script>
```

app.js

```javascript
console.log("Bonjour depuis un fichier externe");
```

---

# Pourquoi préférer un fichier externe ?

Avantages :

- Code plus organisé
- Réutilisable
- Maintenance facilitée
- Collaboration plus simple

---

# Bonnes pratiques

✓ Un fichier JS par fonctionnalité

✓ Nom de fichier explicite

Exemple :

```text
user.js
auth.js
dashboard.js
```

✓ Éviter les noms :

```text
test.js
aaa.js
final2.js
```

---

# Exemple complet

index.html

```html
<!DOCTYPE html>
<html>
<head>
    <title>Formation JS</title>
</head>
<body>

<h1>JavaScript</h1>

<script src="app.js"></script>

</body>
</html>
```

app.js

```javascript
console.log("Formation JavaScript");
```

---

# Exercice 1

Créer un programme affichant :

```text
Bienvenue dans JavaScript
```

---

# Correction

```javascript
console.log("Bienvenue dans JavaScript");
```

---

# Exercice 2

Créer un fichier :

```text
index.html
app.js
```

Puis afficher votre prénom dans la console.

---

# Correction

```javascript
console.log("Joel");
```

---

# À retenir

✓ JavaScript peut être intégré dans HTML

✓ Le fichier externe est recommandé

✓ console.log() permet l'affichage

✓ Commencer par des programmes simples

---

# Test de niveau

## QCM

1. Quelle fonction affiche un message ?

a) print()
b) console.log()
c) echo()

Réponse : b

---

2. Quelle méthode est recommandée ?

a) Script interne
b) Script externe
c) Les deux

Réponse : b

---

3. Quelle extension possède un fichier JavaScript ?

Réponse :

.js
