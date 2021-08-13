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

?????? ERROR: ET http://forkify-api.herokuapp.com/images/PizzaMonkeyBread67f8.jpg net::ERR_BLOCKED_BY_RESPONSE.NotSameOriginAfterDefaultedToSameOriginByCoep

\***\*\*\*\*** : <img src="${recipeData.imageURL}" alt="${recipeData.title}" class="recipe__img" crossorigin/> instead of: <img src="${recipeData.imageURL}" alt="${recipeData.title}" class="recipe__img"/>

\***\*\*\*\*** issues importing icons

        // import icons from '../img/icons.svg'; // Parcel 1
        // import icons from 'url:../../img/icons.svg'; // Parcel 2
        import icons from 'url:../img/icons.svg'; // working version

install polyfillers

        polyfilling async await
            npm i regenerator-runtime

        polyfiling everything else
            npm i core-js

        import at top of controller file

## 284. Listening For load and hashchange Events

some stuff kind of works

## 285 the MVC Architecture

    MODEL:
        buisness logic
        state
        http library

    CONTROLLER:
        application logic
        bridge between model and views(which don't know about one another)
        handles UI events and dispatches tasks to model and view

    VIEW:
        presentation logic

## 286 Refactoring for MVC

create files

        in src/js touch model.js
        in js mkdir views
            in it touch recipeVies.js

        import model into controllers:
            import * as model from '../model.js';

        ???????? nothing rendering riht
        ****** accidentally passed date instead of data into render fn in recipeViews
