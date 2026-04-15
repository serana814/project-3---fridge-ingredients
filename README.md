# Project 3 - Fridge Finder

## What This App Does
A recipe finder where you enter an ingredient and see a bunch of options of meals you can make with it.
The data comes from [TheMealDB API](https://www.themealdb.com/api/json/v1/1/).

## Iteration 1 Learning Log

**What does the API response look like?**
The API gives me a JSON object with an array of meals. Each meal is given a name (strMeal), a photo (strMealThumb), and its own unique ID (idMeal). For the display cards, I used the name and photo for each recipe.

**What was confusing or new?**
I was struggling to understand the .then() chaining after fetch(). I had never seen it before. I did not realize that you needed to first call .json() on the response before you are actually able to read the data. I used the console to help me see what was coming back from the API.

**What did you get working?**
I managed to get the search bar to work. It calls the TheMealDB API and gives you cards that show recipes and images based on the ingredient that you type in.