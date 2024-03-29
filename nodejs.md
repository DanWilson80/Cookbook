NODEJS Installation and Use - Locally and Using GoormIDE
======
Including Use with MongoDB both Locally and Using MongoDB Atlas
------

### Index  
  
[NodeJS](#NodeJS)  
[To be Finished](#TBF)  
[GoormIDE](#GoormIDE)  
[MongoDB_on GoormIDE](#MongoDB_GoormIDE)  
[MongoDB_Locally](#MongoDB_Locally)  
  
  
### Complete Guide to setting up NodeJS and MongoDB Locally is located [here](https://zarkom.net/blogs/linux-ubuntu-local-coding-environment-1528)  
  
NodeJS
------  

* Install NodeJS by following instructions at https://github.com/nodesource/distributions/blob/master/README.md#debinstall

* On beginning a project enter the `Project Folder` using the command line and use `npm init` to initialise `npm` (Node Package Manager) and create the `package.json` file

* Create `app.js` file 

* Install `NPM Modules` by using the following command inside the project folder `npm install (or i) [module name] --save (the save command writes the module to the `package.json` file)

* Uninstall `NPM Modules` (if a module is not working correctly then an uninstall and reinstall to a newer version may help) use the following command `npm uninstall [module name]`

* Call the `npm modules` in the `app.js` file eg: 
```
const express = require("express"),
const	app = express(),
```
which calls the `express` module for use within an app.

* The syntax when calling modules within an app can also be applied as such:
```
const express =    require("express"),
			app =        express(),
			mongoose =   require('mongoose'),
			request =    require("request"),
			bodyParser = require("body-parser");
```
There is no need to use `const` for each variable when using a `,` instead of a `;` at the end of each line. The `"require"` part of each line can also be lined up for the purposes of easier to read code although this is a matter of preference.  
  
[Index](#Index)  
  
### TBF  
**_To Be Finished_**  

*There is more information stored within the readme.md file within my projects on GoormIDE that I need to transcribe over which will be useful to have in one place*  
  
[Index](#Index)  
  
GoormIDE
------
### _TBF - To Be Finished_ 

### How to configure Server in GoormIDE for use with NodeJS  

1. Go to your GoormIDE and `Project/Running URL and Port` this will bring up a window. Enter any name for your `URL` for the server you are creating then enter `3000` as the `Port Number` and click `Register`  
2. Add this code to the bottom of your `app.js` file to enable the server:
```
app.listen(3000, () => {
	console.log("Server listening on Port 3000");
});
```
3. Locate your `HTML File` and open it into the editor then back to `Project => Running URL and Port` then click on the link for the Server that you created and it will open up the `HTML File` in your browser.  

### How to Preview HMTL files in GoormIDE  

1. Go to your GoormIDE and `Project/Running URL and Port` this will bring up a window. Enter any name for your `URL` for the server you are creating then enter `8000` as the `Port Number` and click `Register`  
2. At the command line type `python -m SimpleHTTPServer` and you should get a message stating `Serving HTTP 0.0.0.0 Port 8000...`  
3. Locate your `HTML File` and open it into the editor then back to `Project => Running URL and Port` then click on the link for the Server that you created and it will open up the `HTML File` in your browser.
  
[Index](#Index)  
  
MongoDB_GoormIDE  
------

* When connecting to `MongoDB` the following code is what I used while operating within GoormIDE with MongoDB installed within the IDE:
```
mongoose.connect("mongodb://localhost:27017/yelp_camp", {
	useNewUrlParser: true,
	useCreateIndex: true
}).then(() => {
	console.log("Connected to DB!");
}).catch(err => {
	console.log("ERROR:", err.message);
});
```
Don't forget to add the `mongoose npm` and call the `const = require("mongoose");` variable

* When using `MongoDB Atlas` instead of a local DB I used the following code to access the Atlas DB:
```
mongoose.connect(process.env.MONGOLAB_URI, {
	useNewUrlParser: true,
	useCreateIndex: true
}).then(() => {
	console.log("Connected to DB!");
}).catch(err => {
	console.log("ERROR:", err.message);
});
```
the `process.env.MONGOLAB_URI` references to the `.env` file containing the login details for the Atlas Container. To enable the use of `.env` the `dotenv module` must be installed and `dotenv.config();` must be called below the installed module variables (which must include `const dotenv = require(dotenv)` of course) this allows the connection string for Atlas to be replaced with the variable named within the `.env` file.  
  
[Index](#Index)    
  
MongoDB_Locally  
------  
  
**To install `MongoDB` locally use the following commands**
   1. `killall mongod`
   2. `sudo apt-get purge -y mongodb-org*`
   3. `sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5`
   4. `echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.6 multiverse" | sudo tee     /etc/apt/sources.list.d/mongodb-org-3.6.list`
   5. `sudo apt-get update`
   6. `sudo apt-get install -y mongodb-org`
   7. `rm -rf mongod`
   8. `echo "mongod --dbpath=data --nojournal" > mongod`
   9. `chmod a+x mongod`
   10. `rm -rf data`
   11. `mkdir data`
   12. `./mongod`  (to run the Daemon)
   13. Open a new terminal tab
   14. `mongo` to run the DB
  
[Index](#Index)

