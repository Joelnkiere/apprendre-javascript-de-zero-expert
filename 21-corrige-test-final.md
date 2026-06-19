# Corrigé du Test Final

## À destination du formateur uniquement

⚠️ Ne pas distribuer avant l'évaluation.

---

# Corrigé Partie 1

1. let

2. String

3. ===

4. &&

5. for

6. function

7. Une chaîne de caractères

8. Retourner une valeur

9. ??

10. Number()

---

# Corrigé Partie 2

Exercice 1

```text
Majeur
```

---

Exercice 2

```text
105
```

---

Exercice 3

```text
15
```

---

Exercice 4

```text
1
2
3
```

---

Exercice 5

```text
8
```

---

# Corrigé Projet

```javascript
let nom =
    prompt("Nom");

let note =
    Number(prompt("Note"));

let mention;

if(note >= 18){
    mention = "Excellent";
}
else if(note >= 16){
    mention = "Très Bien";
}
else if(note >= 14){
    mention = "Bien";
}
else if(note >= 10){
    mention = "Passable";
}
else{
    mention = "Échec";
}

alert(
    nom +
    " : " +
    mention
);
```
