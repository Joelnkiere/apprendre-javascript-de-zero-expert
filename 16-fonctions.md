# Module 16 : Les Fonctions en JavaScript 

## Objectifs

À la fin de ce module, vous serez capable de :

* Comprendre le rôle des fonctions
* Créer différents types de fonctions
* Utiliser les paramètres
* Utiliser les valeurs de retour
* Comprendre les callbacks
* Comprendre les closures
* Utiliser les fonctions modernes ES6+
* Manipuler les fonctions d'ordre supérieur
* Utiliser map(), filter() et reduce()

---

# Introduction

Une fonction est un bloc de code réutilisable.

Elle permet :

* d'éviter les répétitions
* d'organiser le code
* de rendre les programmes plus lisibles

On peut comparer une fonction à une machine.

* Elle reçoit éventuellement des données en entrée.
* Elle effectue un traitement.
* Elle renvoie éventuellement un résultat.

Les fonctions sont l'un des éléments les plus importants de JavaScript. Elles sont utilisées dans pratiquement toutes les applications web modernes.

---

# Pourquoi utiliser des fonctions ?

Sans fonction :

```javascript
console.log("Bonjour Joel");
console.log("Bonjour Sarah");
console.log("Bonjour David");
```

Le même code est répété plusieurs fois.

Avec fonction :

```javascript
function saluer(nom){
    console.log("Bonjour " + nom);
}

saluer("Joel");
saluer("Sarah");
saluer("David");
```

Ici, une seule fonction est créée puis réutilisée autant de fois que nécessaire.

Les avantages sont :

* moins de répétition
* code plus facile à maintenir
* meilleure organisation

---

# 1. Function Declaration

## Définition

Une Function Declaration est la manière classique de créer une fonction.

Elle est déclarée avec le mot-clé :

```javascript
function
```

Syntaxe :

```javascript
function saluer(){

    console.log("Bonjour");

}
```

Dans cet exemple :

* `saluer` est le nom de la fonction
* les parenthèses contiennent les paramètres éventuels
* les accolades contiennent les instructions à exécuter

---

## Appel

Créer une fonction ne l'exécute pas automatiquement.

Pour l'utiliser, il faut l'appeler :

```javascript
saluer();
```

Résultat :

```text
Bonjour
```

---

# Hoisting

## Définition

Le hoisting est un mécanisme interne de JavaScript.

Avant d'exécuter le programme, JavaScript analyse le code et prépare certaines déclarations.

Pour les Function Declarations, cela signifie que la fonction peut être appelée avant sa définition dans le fichier.

```javascript
saluer();

function saluer(){
    console.log("Bonjour");
}
```

Ce code fonctionne.

---

## Pourquoi cela fonctionne ?

Lors de la phase de préparation du code, JavaScript enregistre la fonction :

```javascript
function saluer(){
    console.log("Bonjour");
}
```

La fonction est donc déjà connue lorsque :

```javascript
saluer();
```

est exécuté.

---

## Attention

Le hoisting ne signifie pas que le code est déplacé physiquement.

C'est simplement le moteur JavaScript qui prépare certaines déclarations avant l'exécution.

---

# 2. Paramètres

## Définition

Les paramètres sont des variables spéciales déclarées entre les parenthèses d'une fonction.

Ils permettent à la fonction de recevoir des données provenant de l'extérieur.

```javascript
function addition(a,b){

    return a+b;

}
```

Ici :

```javascript
a
```

et

```javascript
b
```

sont les paramètres.

---

## Exemple

```javascript
addition(10,5);
```

Lors de l'appel :

```javascript
a = 10
b = 5
```

La fonction effectue alors le calcul :

```javascript
10 + 5
```

---

## Pourquoi utiliser des paramètres ?

Sans paramètres :

```javascript
function addition(){

    return 10 + 5;

}
```

La fonction retourne toujours le même résultat.

Avec des paramètres, elle devient réutilisable pour différentes valeurs.

---

# Plusieurs paramètres

Une fonction peut recevoir plusieurs informations.

```javascript
function calculerMoyenne(
    note1,
    note2,
    note3
){

    return (
        note1 +
        note2 +
        note3
    ) / 3;

}
```

Cette fonction reçoit trois notes puis calcule leur moyenne.

---

# Paramètres par défaut

## Définition

Les paramètres par défaut permettent d'attribuer automatiquement une valeur lorsqu'aucun argument n'est fourni.

```javascript
function saluer(
    nom = "Invité"
){

    console.log(
        "Bonjour " + nom
    );

}
```

---

## Exemple

```javascript
saluer();
```

Résultat :

```text
Bonjour Invité
```

Si aucune valeur n'est fournie, JavaScript utilise la valeur par défaut.

---

# 3. Valeur de Retour

## Définition

Une fonction peut produire un résultat.

Pour renvoyer ce résultat, on utilise le mot-clé :

```javascript
return
```

```javascript
function carre(nombre){

    return nombre * nombre;

}
```

---

## Pourquoi utiliser return ?

Sans `return`, le résultat reste à l'intérieur de la fonction.

Avec `return`, le résultat peut être récupéré et utilisé ailleurs dans le programme.

---

## Utilisation

```javascript
let resultat =
    carre(5);

console.log(resultat);
```

Résultat :

```text
25
```

---

# Retour d'un Objet

Une fonction peut retourner un objet.

```javascript
function creerUtilisateur(){

    return {
        nom: "Joel",
        age: 25
    };

}
```

---

# Retour d'un Tableau

Une fonction peut également retourner un tableau.

```javascript
function obtenirNotes(){

    return [
        10,
        15,
        18
    ];

}
```

---

# 4. Scope (Portée)

## Définition

La portée (scope) détermine où une variable peut être utilisée dans le programme.

Certaines variables sont accessibles partout.

D'autres ne sont accessibles que dans une fonction ou un bloc spécifique.

---

## Scope Local

Une variable déclarée dans une fonction est locale à cette fonction.

```javascript
function test(){

    let message =
        "Bonjour";

}
```

---

Impossible d'accéder à :

```javascript
message
```

à l'extérieur.

Cela protège les données et évite les conflits entre variables.

---

## Scope Global

Une variable globale est déclarée en dehors des fonctions.

```javascript
let pays = "RDC";

function afficher(){

    console.log(pays);

}
```

La fonction peut accéder à cette variable.

---

# 5. Function Expression

## Définition

Une Function Expression est une fonction stockée dans une variable.

```javascript
const addition =
    function(a,b){

        return a+b;

    };
```

Ici, la fonction est affectée à la variable :

```javascript
addition
```

---

## Utilisation

```javascript
addition(5,3);
```

---

# Différence avec Function Declaration

Les Function Expressions ne bénéficient pas du même hoisting que les Function Declarations.

```javascript
addition(1,2);

const addition =
    function(a,b){
        return a+b;
    };
```

Erreur.

Pourquoi ?

Parce que la variable `addition` n'est pas encore disponible au moment de l'appel.

---

# 6. Named Function Expression

## Définition

Une Named Function Expression est une Function Expression qui possède un nom interne.

```javascript
const calcul =
    function addition(a,b){

        return a+b;

    };
```

Le nom :

```javascript
addition
```

existe uniquement à l'intérieur de la fonction.

Cette technique est parfois utilisée pour le débogage.

---

# 7. Fonctions Anonymes

## Définition

Une fonction anonyme est une fonction sans nom.

```javascript
function(){

}
```

Elle est souvent utilisée lorsqu'une fonction n'a besoin d'être utilisée qu'une seule fois.

---

Très utilisée avec :

```javascript
setTimeout(
    function(){

        console.log(
            "Bonjour"
        );

    },
    1000
);
```

Ici, la fonction est exécutée après une seconde.

---

# 8. Arrow Functions

## Définition

Les Arrow Functions ont été introduites avec ES6.

Elles permettent d'écrire des fonctions de manière plus concise.

---

## Syntaxe

```javascript
const addition =
    (a,b) => {

        return a+b;

    };
```

Le symbole :

```javascript
=>
```

est appelé flèche (arrow).

---

## Retour implicite

Lorsqu'une seule expression est retournée, le mot-clé `return` peut être omis.

```javascript
const addition =
    (a,b) => a+b;
```

---

## Un seul paramètre

```javascript
const carre =
    n => n*n;
```

Les parenthèses deviennent facultatives.

---

## Aucun paramètre

```javascript
const bonjour =
    () => {

        console.log(
            "Bonjour"
        );

    };
```

---

# Comparaison

Function Declaration

```javascript
function carre(n){

    return n*n;

}
```

Arrow Function

```javascript
const carre =
    n => n*n;
```

Les deux produisent le même résultat.

L'Arrow Function est simplement plus compacte.

---

# 9. Rest Parameters

## Définition

Les Rest Parameters permettent de récupérer un nombre illimité d'arguments.

```javascript
function somme(
    ...nombres
){

    console.log(
        nombres
    );

}
```

Le symbole :

```javascript
...
```

regroupe toutes les valeurs dans un tableau.

---

## Exemple

```javascript
somme(
    10,
    20,
    30,
    40
);
```

Résultat :

```javascript
[10, 20, 30, 40]
```

---

# Cas pratique

```javascript
function somme(
    ...nombres
){

    return nombres.reduce(
        (acc,n) =>
            acc+n,
        0
    );

}
```

Cette fonction peut additionner autant de nombres que nécessaire.

---

# 10. Callback Functions

## Définition

Un callback est une fonction passée en argument à une autre fonction.

La fonction qui reçoit le callback pourra l'exécuter plus tard.

---

## Exemple

```javascript
function executer(
    callback
){

    callback();

}
```

---

Utilisation :

```javascript
executer(
    function(){

        console.log(
            "Exécuté"
        );

    }
);
```

---

# Pourquoi les Callbacks ?

Les callbacks sont très utilisés pour :

* les événements utilisateur
* les requêtes API
* React
* Node.js
* les opérations asynchrones

Exemple :

Lorsqu'un utilisateur clique sur un bouton, une fonction est exécutée automatiquement.

---

# 11. Fonctions d'Ordre Supérieur

## Définition

Les fonctions d'ordre supérieur (Higher Order Functions) sont des fonctions qui :

* reçoivent une fonction en paramètre
* ou retournent une fonction

---

## Pourquoi sont-elles importantes ?

Elles permettent de créer du code plus flexible et réutilisable.

---

## Exemple

```javascript
function calcul(
    a,
    b,
    operation
){

    return operation(
        a,
        b
    );

}
```

---

Utilisation

```javascript
calcul(
    10,
    5,
    (a,b) => a+b
);
```

La fonction reçue détermine l'opération à effectuer.

---

# 12. Closures

## Définition

Une closure est une fonction qui conserve l'accès aux variables de son environnement même après la fin de l'exécution de la fonction externe.

C'est un concept fondamental en JavaScript.

---

## Exemple

```javascript
function compteur(){

    let valeur = 0;

    return function(){

        valeur++;

        return valeur;

    };

}
```

---

Utilisation

```javascript
const c =
    compteur();

console.log(c());
console.log(c());
console.log(c());
```

---

Résultat

```text
1
2
3
```

---

# Pourquoi ?

La fonction interne conserve l'accès à :

```javascript
valeur
```

même après la fin de la fonction externe.

La variable n'est donc pas détruite.

Cela permet de créer des données privées et persistantes.

---

# 13. Fonctions Récursives

## Définition

Une fonction récursive est une fonction qui s'appelle elle-même.

---

## Pourquoi utiliser la récursivité ?

Elle est utile pour résoudre des problèmes répétitifs :

* parcours d'arbres
* menus imbriqués
* calculs mathématiques

---

## Exemple

```javascript
function compteARebours(n){

    if(n === 0){
        return;
    }

    console.log(n);

    compteARebours(
        n - 1
    );

}
```

---

Utilisation

```javascript
compteARebours(5);
```

---

Résultat

```text
5
4
3
2
1
```

---

# Exemple : Factorielle

```javascript
function factorielle(n){

    if(n === 1){
        return 1;
    }

    return n *
        factorielle(n-1);

}
```

La fonction continue à s'appeler jusqu'à atteindre le cas d'arrêt.

---

# 14. IIFE

## Définition

IIFE signifie :

```text
Immediately Invoked Function Expression
```

C'est une fonction exécutée immédiatement après sa création.

---

## Pourquoi utiliser une IIFE ?

Avant l'arrivée des modules JavaScript, elles étaient utilisées pour éviter de polluer l'espace global.

---

```javascript
(function(){

    console.log(
        "Bonjour"
    );

})();
```

---

Version Arrow

```javascript
(() => {

    console.log(
        "Bonjour"
    );

})();
```

---

# 15. Méthodes d'Objets

## Définition

Lorsqu'une fonction appartient à un objet, on parle généralement de méthode.

```javascript
const utilisateur = {

    nom : "Joel",

    saluer(){

        console.log(
            "Bonjour"
        );

    }

};
```

---

Utilisation

```javascript
utilisateur.saluer();
```

---

# 16. Le Mot-Clé this

## Définition

Le mot-clé :

```javascript
this
```

représente généralement l'objet qui exécute la méthode.

---

```javascript
const utilisateur = {

    nom : "Joel",

    afficher(){

        console.log(
            this.nom
        );

    }

};
```

---

Résultat

```text
Joel
```

Ici :

```javascript
this.nom
```

fait référence à :

```javascript
utilisateur.nom
```

---

# 17. map()

## Définition

La méthode `map()` permet de transformer chaque élément d'un tableau.

Elle retourne un nouveau tableau.

---

```javascript
const nombres =
    [1,2,3];

const doubles =
    nombres.map(
        n => n*2
    );
```

---

Résultat

```javascript
[2,4,6]
```

Chaque valeur est multipliée par deux.

---

# 18. filter()

## Définition

La méthode `filter()` permet de sélectionner certains éléments d'un tableau.

Elle retourne un nouveau tableau contenant uniquement les éléments qui respectent une condition.

---

```javascript
const nombres =
    [1,2,3,4,5];

const pairs =
    nombres.filter(
        n => n%2===0
    );
```

---

Résultat

```javascript
[2,4]
```

Seuls les nombres pairs sont conservés.

---

# 19. reduce()

## Définition

La méthode `reduce()` permet de réduire un tableau à une seule valeur.

Cette valeur peut être :

* une somme
* une moyenne
* un objet
* une chaîne de caractères

---

```javascript
const nombres =
    [1,2,3,4];

const somme =
    nombres.reduce(
        (acc,n)=>
            acc+n,
        0
    );
```

---

Résultat

```javascript
10
```

---

## Comprendre les paramètres

Dans :

```javascript
(acc,n) => acc+n
```

* `acc` représente l'accumulateur
* `n` représente la valeur courante

À chaque étape, l'accumulateur conserve le résultat précédent.

---

# Projet de Fin de Module

Créer une application permettant :

* d'enregistrer plusieurs notes
* de calculer la moyenne
* d'afficher la mention
* d'utiliser :

  * une fonction classique
  * une arrow function
  * reduce()

---

# À retenir

✓ Function Declaration

✓ Function Expression

✓ Named Function Expression

✓ Arrow Function

✓ Paramètres par défaut

✓ Rest Parameters

✓ Callback Functions

✓ Higher Order Functions

✓ Closures

✓ Récursivité

✓ IIFE

✓ this

✓ map()

✓ filter()

✓ reduce()

---

# Test de Niveau

## Partie 1 : Théorie

1. Quelle différence existe entre une Function Declaration et une Function Expression ?

2. À quoi sert return ?

3. Qu'est-ce qu'une Closure ?

4. Qu'est-ce qu'un Callback ?

5. Que fait reduce() ?

---

## Partie 2 : Exercices

### Exercice 1

Créer une fonction qui calcule l'aire d'un cercle.

---

### Exercice 2

Créer une Arrow Function qui calcule le cube d'un nombre.

---

### Exercice 3

Créer une fonction utilisant Rest Parameters pour additionner un nombre illimité de valeurs.

---

### Exercice 4

Créer une fonction récursive qui calcule la somme des nombres de 1 à n.

---

### Exercice 5

À partir du tableau suivant :

```javascript
const notes = [10, 12, 15, 18, 8];
```

Utiliser :

* map()
* filter()
* reduce()

pour effectuer différents traitements.
