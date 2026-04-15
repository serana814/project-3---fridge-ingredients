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

## Iteration 2 Learning Log

**How did you connect user input to API calls?**
When anyone types an ingredient in the search bar and clicks the search button, the code automatically uses document.ElementById to take the value from the input box. Then, that value is automatically inserted into the API URL. So, if you type in the word "chicken", it automatically builds the URL with chicken in it and gets you results that are specifically containing that ingredient. Each time you search it creates a new API call with whatever you typed into the search bar. 

**What CSS layout did you use for displaying data?**
I used CSS grid to display the the meal cards in a grid. The auto-fill and minmax properties are what allow the grid to be responsive. This means that the number of columns displayed on the screen depends on how wide the screen is (more columns on a wider screen and less columns on a more narrow screen). 

**What design decisions did you make?**
I decided to use a pop up whenever someon clicks on a recipe. Whenever someone clicks on a recipe, a pop up will appear with the image of the recipe, the ingredients, and the directions. This allows the user to click on an recipe, see the details and decide if they want to use it and if not, go back to where they left off on the recipes page. The rest of the design is very minimal as i believed that it would be too chaotic with the images of the recipes if I were to add more designs or colors. I also decided to include a loading message so that while the user waits, they know that something is happening and don't assume that the website is not working. 