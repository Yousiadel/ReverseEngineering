# ReverseEnginnering
Models Folder:

The next folder is the model folder, which has a index.js file and a user.js file. The index.js file uses the models that are in the model folder (in this case, user). 

The user model (in user.js) sets up the sequelize table for the email and password for the user.

A user will be an object compiled of an email that is a string, unique, and is a valid email as well as a password, which is also a string.  There is a custom model for validating password which we saw linked in the passport.js file.

Lastly, there is a “addHook” function, which is an automatic method that is run. This one is run before a user is created, and will automatically hash their password.

Hashing the password refers to scrambling the password through a random algorithm. This is done for security purposes and so a user’s password isn’t stored directly.

Public Folder:

The public folder includes everything needed for the front end of this application.  There are three different HTML files for the login, members, and signup pages (login.html, members.html, and signup.html). These files refer to the CSS and JS files. The js folder includes three different js files (login.js, members.js, and signup.js) which is the script needed for these HTML files.

The style.css file in stylesheets folder simply has a top margin for the forms.

Routes Folder:

The routes folder includes two files, api-routes.js and html-routes.js. 

The api routes include the POST and GET routes that allow for a user to be signed up and their information stored in the database.  

The html routes render the html pages. The GET requests are needed so that different things will happen if the user already has an account (sent to member page) or doesn’t have an account (sent to sign up page).

Package.json

Includes that information for the development of this project called “1-Passport-Example”. The required dependencies for this project are:
•	Bcryptjs - uses an API to get random numbers for the hashing of passwords
•	Express
•	Express-session
•	Mysql2
•	Passport - authentication middleware
•	Passport-local
•	Sequelize

