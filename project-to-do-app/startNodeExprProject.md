# Starting a coding project with Node and Express

STEP | EXPLANATION
:---- | :---------
Create a folder for the project on your computer | You need an empty folder with the name of your project.
Open the folder with Visual Studio Code | In VSC, go to File – Open and then go to the directory where you created your project folder and open it.
Open the terminal of VSC | In VSC, go to View – Terminal. On Mac, the shortcut is Ctrl ` (backtick). If you prefer, you can use a terminal outside of VSC.
Check if you have Node installed | In the terminal, type `node –-version`. If Node is installed, you will see the version in your terminal. If not, then go to nodejs.org to download it.
Check if you have npm installed | In the terminal, type `npm –version` (or: `npm -v`) and you will see if npm is installed. If not, get npm from npmjs.com.
Initite your project | In the terminal, type `npm init`. You will see all sorts of text rolling in your terminal. At a certain moment, there will be questions in the terminal, such as: the project's name, the project's initial version, the project's description, etc. You can skip all of these questions: just click enter all the time. You will see that a file called package.json has been created after this.
Main file or entry point | If you do not change anything during `npm init`, and just skip through the questions, then npm will automatically decide that index.js is your main file (entry point).
The npm package manager: **package.json**. | You need this file to set up the Node modules that you need. You do not have to look at those, the programme will use any modules it needs automatically. Install all Node modules with the command `npm i` (or `npm install`). You will see that a package-lock.json file is created automatically in the project folder. 
Install Express | Install Express for **each new project**: `npm i express -–save`
Import Express in your main file (entry point) | To be able to use Express with Node, you have to import it in your main file. Create the file and call it index.js. Put at the top of your index.js file: ```const express = require(“express”) const app = express()```
Add port to index.js (main file) | At the bottom of your index.js file, add the app listener with the port. You can do this in various ways. For a fixed port: `app.listen(3000, () {console.log(“Listening on port 3000”) })` In case of flexibility (port can change): `app.listen(port, () => { console.log(`Listening on port ${port}.`) })` To use this way of indicating the port, you have to define the port in your code, for example at the top: `const port = 3000`.
Run your code from the terminal | Use the command `node index.js` to run your code.
Check localhost in your browser | Go to your browser and type localhost:3000 as url. If all went well, you will see in your terminal the text you put for the listener (for example, Listening on port 3000).
Install nodemon | To avoid having to kill and restart the server every time you make a change in the code, you can use the Nodemon package: `npm install –save-dev nodemon`. This should add nodemon to your package.json file. Add a script to this file: `"start": "nodemon index.js"`. Whenever changes are made to the code, nodemon will automatically restart the server.