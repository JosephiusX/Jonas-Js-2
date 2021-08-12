# Jonas-Js-2

## sec 18 L. 282 Loading a Recipe from API

open new project in directory

    npm init -y
    remove main property from package.json(to avoid later error)

setup scripts

    "start": "parcel index.html"
    "build": "parcel build index.html"

install parcel as dev dependancy

    npm i parcel@next -D
    npm i
    npm start

project api documentation

    https://forkify-api.herokuapp.com/v2

        get recipe url:
            https://forkify-api.herokuapp.com/api/v2/recipes/5ed6604591c37cdc054bc886
        we use this to make a fetch in controller.js

        try with a different id
            5ed6604691c37cdc054bd0c0

## 283. Rendering the Recipe

?????? ERROR: ET http://forkify-api.herokuapp.com/images/PizzaMonkeyBread67f8.jpg net::ERR_BLOCKED_BY_RESPONSE.NotSameOriginAfterDefaultedToSameOriginByCoep ****\***** : <img src="${recipeData.imageURL}" alt="${recipeData.title}" class="recipe__img" crossorigin/> instead of: <img src="${recipeData.imageURL}" alt="${recipeData.title}" class="recipe__img"/>
