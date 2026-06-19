# Module 14 : Les Boucles

## Objectifs

- Répéter des instructions
- Utiliser while
- Utiliser do...while
- Utiliser for
- Éviter les boucles infinies

---

# Pourquoi les boucles ?

Éviter de répéter le même code.

Mauvaise pratique :

```javascript
console.log(1);
console.log(2);
console.log(3);
console.log(4);
console.log(5);
```

---

# Boucle while

Syntaxe :

```javascript
while(condition){
}
```

---

# Exemple

```javascript
let i = 1;

while(i <= 5){
    console.log(i);
    i++;
}
```

---

# Résultat

```text
1
2
3
4
5
```

---

# do...while

Exécute au moins une fois.

```javascript
let i = 1;

do{
    console.log(i);
    i++;
}
while(i <= 5);
```

---

# Boucle for

La plus utilisée.

```javascript
for(
    let i = 1;
    i <= 5;
    i++
){
    console.log(i);
}
```

---

# Parcourir les nombres pairs

```javascript
for(
    let i = 2;
    i <= 20;
    i += 2
){
    console.log(i);
}
```

---

# Boucles imbriquées

```javascript
for(let i=1;i<=3;i++){

    for(let j=1;j<=3;j++){

        console.log(i,j);

    }

}
```

---

# Exemple : Table de multiplication

```javascript
for(let i=1;i<=10;i++){

    console.log("5 x " + i +
        " = " + (5*i));

}
```

---

# Erreur fréquente

```javascript
while(true){

}
```

Boucle infinie.

---

# Projet

Afficher :

```text
Étudiant 1
Étudiant 2
...
Étudiant 10
```

---

# Exercices

## Exercice 1

Afficher de 1 à 20.

---

## Exercice 2

Afficher les nombres pairs de 2 à 50.

---

## Exercice 3

Afficher la table de multiplication de 7.

---

# Corrigés

## Correction Exercice 1

```javascript
for(let i=1;i<=20;i++){
    console.log(i);
}
```

---

## Correction Exercice 2

```javascript
for(let i=2;i<=50;i+=2){
    console.log(i);
}
```

---

## Correction Exercice 3

```javascript
for(let i=1;i<=10;i++){
    console.log(7*i);
}
```

---

# À retenir

✓ while répète tant que la condition est vraie

✓ do...while s'exécute au moins une fois

✓ for est la boucle la plus utilisée

✓ Attention aux boucles infinies

---

# Test de niveau

## QCM

1. Quelle boucle s'exécute au moins une fois ?

---

2. Quelle boucle est la plus utilisée ?

---

3. Quel risque existe avec une mauvaise condition ?

---

## Défi

Afficher tous les nombres de 100 à 1 dans l'ordre décroissant.
