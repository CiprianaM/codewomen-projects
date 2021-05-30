## Project Advice Generator

### The goal of this project is to practice working with an API

We will use HTML, CSS, JavaScript and the Advice Slip JSON API for our project (https://api.adviceslip.com/#top).

**Basic functionality:** we want our programme to generate a new advice whenever the user presses the button. A very simple example looks like this:  

<img src="/project_advice_generator/exampleAdviceGenerator.png" width="600" />


### For starters

1. Create a new folder on your local computer with the name: project-advice-generator
1. Create an index.html file with the general template code
1. Create a style.css file and add this to your HTML file as `<link>` (check how to add CSS to an HTML file)
1. Make sure you have *Advice Generator* as the title (this will show in the tab when your app runs in the browser)
1. Build the page according to the example
1. If you want to challenge yourself, try to make the page more attractive


### For more advanced students

**Basic setup (without API requests):**

1. Create a new folder on your local computer with the name: project-advice-generator
1. Create an index.html file with the general template code
1. Create a main.js file. Copy the array with strings from the `testAdvice.js` file and paste it at the top of your main.js file
1. Create a style.css file
1. Use the class names from the HTML file in your CSS
1. Link the JavaScript file to the HTML document so that the JavaScript code will be able interact with the HTML document
1. Add a link to the css file in the HTML
1. Add **Advice Generator** within the `<title>` tags
1. Add an `<h1>` element with the name of your app as the first element in the `<body>`
1. Create a `<div>` element with class name of `advice-display`
1. Add a `<button>` element with class name `advice-button`
1. The `main.js` file contains an array of strings that you can use for testing the javascript functionality before you start working with the API
1. The app should always start with a welcome page, also after refresh. The advice texts should only show up when the button is clicked.
1. Write the function `newAdvice()` that generates a random whole number that ranges from 0 to the length of our advice array
1. Use the number from the previous step as value called `randomNumber` to get a random advice text 
1. Display the content of the random advice into the `advice-display` element
1. Add styling to the style.css file you created 

**Full project, using API requests:**

1. Instead of getting an advice string from the `advice.js` file, you request a random advice using the Advice Slip JSON API (see url at the top of this README)
1. Write a `getAdvice()` function and use this as the onclick attribute for the button
1. The `getAdvice()` function should return a random advice from the Advice Slip JSON API
1. The function should return "Something has gone wrong" if there is an error
1. Show the response data (the advice) in the `advice-display` element
1. Since the Advice Slip endpoint for random advice takes time to reload, you cannot click the button quickly, one time after the other. This will generate the same advice, even though you use the random endpoint. Solve this problem!

**Challenge yourself:**

1. Create an advice for every day of the week
1. Let the advice-display font-size increase or decrease in size depending upon the viewport
1. Let the advice-display box increase or decrease in size depending upon the amount of text
1. Improve the design and layout, make it look good but keep the app responsive


### For graduates

1. Build this project as React app
1. Use create-react-app, create components and write the code for the functionality explained above
1. Challenge yourself: create advice cards that are continuously added and remain on the screen when a new advice is generated
1. Make it into an attractive app

