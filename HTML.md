# Prise en main

## But de la série de vidéo 🎯

Ici, nous allons voir comment créer un site web avec la sainte trinité [HTML](https://fr.wikipedia.org/wiki/Hypertext_Markup_Language), [CSS](https://fr.wikipedia.org/wiki/Cascading_Style_Sheets) ainsi que [JavaScript](https://fr.wikipedia.org/wiki/JavaScript).

Pour commencer, nous allons prendre un challenge disponible sur le site [frontendmentor](https://www.frontendmentor.io/challenges). Plus particulièrement [ce challenge](https://www.frontendmentor.io/challenges/intro-component-with-signup-form-5cf91bd49edda32581d28fd1).

Je vous invite, bien évidemment, à en faire (pleins) d'autres directement depuis le site.

## HTML

Nous allons utiliser le site [w3schools](https://www.w3schools.com/tags/default.asp) pour découvrir le langage HTML. 

Il y a plein de choses à savoir sur le langage HTML. Les balises, les attributs, etc.

```html

<!-- Ceci est un commentaire -->

Voilà une balise HTML :
Une balise HTML est un bloc de code qui permet de représenter un élément de la page web.

Elle est définie par une balise ouvrante <p> et une balise fermante </p>.
```

Il y a plein d'autres balises, mais pour l'instant, nous avons seulement vu comment créer un paragraphe.

L'une des balises les plus utilisées est la balise `<div>`. Elle permet de créer des blocs de contenu.

Nous avons aussi vu comment avoir une structure de page validé avec le [w3c](https://validator.w3.org/#validate_by_input) pour `World Wide Web Consortium` 

```html
<!-- La balise DOCTYPE permet de définir mon document comme HTML -->
<!DOCTYPE html>
<!-- La balise <html></html> est la 1er balise qui doit être ouverte -->
<html>
    <!-- La balise <head></head> permet de définir des informations sur mon document -->
<head>
    <!-- La balise <title></title> permet de définir le titre de mon document, c'est la seule balise obligatoire dans la balise <head></head> -->
  <title>Title of the document</title>
</head>

    <!-- La balise <body></body> permet de définir le contenu de mon document -->
<body>
    <!-- Ici, nous avons 2 balises, h1 et p
    
    h1 pour définir un titre
    et p pour un paragraphe
    
    -->
  <h1>This is a heading</h1>
  <p>This is a paragraph.</p>
</body>

</html>
```

### La sémantique

En plus d'être un élément de la page web, les balises HTML peuvent être utilisées pour définir au niveau sémantique quelque chose de plus juste.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Title of the document</title>
  </head>
  <body>
    <div>
      <h1>Mon en-tête</h1>
    </div>
    <div>
      Ma première section de mon site web
    </div>
    <div>
      Ma deuxième section de mon site web
    </div>
    <div>
      Mon pied de page
    </div>
  </body>
</html>
```

Cette structure est juste selon le W3C, mais n'est pas pour autant juste concernant la sémantique.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Title of the document</title>
  </head>
  <body>
    <header>
      <h1>Mon en-tête</h1>
    </header>
    <section>
      Ma première section de mon site web
    </section>
    <section>
      Ma deuxième section de mon site web
    </section>
    <footer>
      Mon pied de page
    </footer>
  </body>
</html>
```

Alors qu'ici, c'est plus juste. Même si l'autre n'est pas faux pour autant 😅.

Nous avons aussi vu les `attributs` qui sont des informations qui sont associées à une balise.

Ex : 

```html
<h1 id="titre">Ceci est mon titre</h1>
<h2 class="sousTitre">Ceci est mon titre</h2>
```

Ici, nous avons un attribut `id` qui est l'identifiant de la balise `h1`.

Et un attribut `class` qui est la classe de la balise `h2`.

Nous avons des attributs dits global, qui sont disponible pour tout le monde comme la balise `id` et `class`. Et d'autres attributs spécifiques à chaque balise.

Plus de détail ici : [w3schools](https://www.w3schools.com/tags/ref_attributes.asp)

## CSS

Toujours grâce à [w3schools](https://www.w3schools.com/css/default.asp) nous avons vu comment créer des styles.

Il y a tellement de choses à savoir sur le CSS. Les propriétés, les valeurs, etc. que nous ne pourrons pas tout voir ici.

C'est pourquoi je vais faire un petit tour d'horizon.

```css

/* Ceci est un commentaire */

/*
  h1 ici est un sélécteur.
  color est une propriété.
  red est une valeur.
*/

h1 {
  color: red;
}
```

Il y a plein d'autres propriétés, mais pour l'instant, nous avons seulement vu comment créer une couleur.

Nous avons aussi vu plus haut l'`id` et la `class`.

Comment en CSS fait ont pour aller récupérer cette information ?

```css
/* Pour un identitiant, nous avons le signe # */

#titre {
  font-size: 10px;
}

/* Pour une classe, nous avons le signe . */

.sousTitre {
  padding: 2em;
}

/* Et plus haut, nous avons vu que je peux directement la balise h1 par exemple */

p {
  color: blue;
}
```

Je peux aussi aller loin dans les sélecteurs, c'est-à-dire que je peux faire des sélecteurs imbriqués.

Ex : 

```html
<section>
  <h1>Mon titre</h1>
  <p id="paragraphe">C'est mon paragraphe avec un 
    <a>lien</a>
  </p>
</section>
```
```css
#paragraphe a {
  color: yellow;
}
```

Ici, nous avons dit 

> "Attention, je veux que mon paragraphe ait un lien qui a la couleur jaune".

Maintenant, si vous souhaitez apprendre le CSS, j'ai plus qu'à vous dire que vous pouvez aller sur [w3schools](https://www.w3schools.com/css/default.asp) et de faire pleiiiiiin de TP pour justement apprendre les bases et de connaître [les balises](https://www.w3schools.com/cssref/default.asp) et les sélecteurs.

## JavaScript

Ah, JavaScript, le langage de programmation pour le web.

Nous allons faire un peut de JS pour le challenge [frontend Mentor](https://www.frontendmentor.io/challenges/intro-component-with-signup-form-5cf91bd49edda32581d28fd1). Je vais pas tout détailler ici car je vais faire une série de vidéo 😁

```js
// Je récupère mon formulaire
var form = document.getElementById("form");

// Je récupère les valeurs qui nous intéresse grâce aux id et class.
var firstName = document.getElementById("firstName");
var lastName = document.getElementById("lastName");
var email = document.getElementById("email");
var password = document.getElementById("pwd");

// Toutes mes infos dans un tableau (représenté par les []).
var formCheck = [firstName, lastName, email, password];

// Je récupère les classes errorDetails
var errorDetails = document.getElementsByClassName("errorDetails");

// À la soumission du formulaire, je lance la fonction
form.addEventListener('submit', function(event) {
  // Ici, grâce à la fonction `event.preventDefault()`, je peux empêcher le comportement par défaut du formulaire qui est de refresh la page.
  event.preventDefault();

  // Nous avons la boucle for qui va parcourir toutes les valeurs du tableau formCheck.
  for(index=0; index < formCheck.length; index++) {
    // Ici, je vais vérifier si la valeur est vide.
    if(!formCheck[index].value) {
      getError(formCheck[index].name, index);
    } else {
      formCheck[index].classList.remove("error");
      errorDetails[index].innerHTML = "";
    }
  }
})

// Je créer une fonction qui va me permettre de vérifier les erreurs.
function getError(property, id) {

  // Switch qui va me permettre de vérifier les erreurs en fonction de la propriété.
  switch (property) {
    case "firstName":
      firstName.classList.add("error");
      errorDetails[id].innerHTML = "First Name cannot be empty";
      break;
    case "lastName":
      lastName.classList.add("error");
      errorDetails[id].innerHTML = "Last Name cannot be empty";
      break;
    case "email":
      email.classList.add("error");
      errorDetails[id].innerHTML = "Looks like this is not an email";
      break;
    case "pwd":
      password.classList.add("error");
      errorDetails[id].innerHTML = "Password cannot be empty";
      break;
    default:
      console.log("Pas de cas concernant cette propriétée.");
  }
}

```

## La playlist vidéo 🎥

⭐️ La [playlist vidéo]() 🎥
Laisser un commentaire sur la vidéo et un 👍 ! ⭐️

## Documentation 🗂

- HTML : https://fr.wikipedia.org/wiki/Hypertext_Markup_Language
- CSS :  https://fr.wikipedia.org/wiki/Cascading_Style_Sheets
- JavaScript : https://fr.wikipedia.org/wiki/JavaScript
- W3Schools : https://www.w3schools.com/
- MDN : https://developer.mozilla.org/fr/docs/Web/
- W3C : https://www.w3.org/
- Frontend Mentor : https://www.frontendmentor.io/
- Frontend Mentor Challenge : https://www.frontendmentor.io/challenges/

---

## Bonus 🚀

Si vous avez des idées et des implémentations supplémentaire, n'hésitez pas à vous amuser... C'est comme ça qu'on apprend ! ❤️

---

# Author

👤 [Anthony Gorski](https://twitter.com/Gorski_anthony)

🏠 [Main Menu](./README.md)