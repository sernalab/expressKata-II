# How to create a express project step by step

## A: Install the back-end
## ----------------------------

### STEP 1º
### Create a folder with a semanthic name

==>  `mkdir expressKata-II`

### STEP 2º
### Initizalize the npm and use the '-y' especification to be faster and create the ***jason package*** file

==>  `npm init --y`

### STEP 3º
### Install npm

Install into the directory (i.e. expressKata-II)

==>  `npm install express --save`

*the ***'-- save'*** especification indicates that the folder to save is the working directory (on the other hand, the ***'-g'*** especification install the package into the globla scope). But the best thing is that you create the jason package file where there is the info to find the dependencies*

## B: Install the front-end
## ----------------------------

### STEP 4º
### Inititialite bower
Initizalize the bower package and use the '-y' especification to be faster and create the ***jason package*** file

==>  `bower init --y`

### STEP 5º
### Install Bower

==>  `sudo npm install bower -g`

*In this case we install bower in the global mode ***'-g'***, for that reason if you work with apple computers you should introduce the ***'sudo'*** command in order to access to the user administration.*

### STEP 6º
### Create a .gitignore file

The *.gitignore'* file should into the main directory in order to use *'github'* copy and maintain clean the repository from the dependencies as *'node_modules'* or *'bower_components'*

==>  `touch gitignore`

### STEP 7º
Introduce into this file the dependencies to avoid be copied into *'github'*:

```
node_modules
bower_components
```

### STEP 8º
### Create a .bowerrc

The *'.bowerrc'* file into the main directory in order to choose the path where copying the bower components.

*'github'* copy and maintain clean the repository from the dependencies as *'node_modules'* or *'bower_components'*

==>  `touch .bowerrc`

### STEP 9º
### Complete the .bowerrc file
Introduce into this file the directory you want to use, for example:

```
{
  "directory": "public/bower_components"
}
```

### STEP 10º
### Install *'the bootstrap librery'*

This librery goes into the working directory using bower install:

==>  `bower install bootstrap --save`

*With ***'--save'*** you write this dependency into the jason package file where there is the info to find the rest os dependencies*


### STEP 11º
### Install *'the pug package'*

This package goes into the working directory using npm istall:

==>  `npm install pug --save`

*With ***'--save'*** you write this dependency into the jason package file where there is the info to find the rest os dependencies*

### STEP 12º
### Create the firs file app.js.

You can use this notation as an example:

```
const express = require("express") // calling express
const app = express()  // defining the function
const PORT = 3000  // choosing a PORT (always uppercase)

app.set("view engine", "pug") // defining dependencies
app.use(express.static("public")) // indicating routes

//root directory

app.get('/', (req, res) => {
    res.render('index')
})

app.listen(PORT, () => console.log('listening port 3000'))
```

### STEP 13º
### Create a 'views' directory

Into this directory create a intex.pug file

`mkdir views`
`cd views`
`touch index.pug`

14º Write somo content into this file as:

h2 This is the first content


### STEP 15ª
### Add a shorcout to call th server

Into the package.json file find this piece code:

```
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
```

and change it whit this other code:

```
 "scripts": {
    "start": "node app.js"
  },
```

whit this change you can call the server quicky via terminal with this command:

`npm start`
now (after call 'npm start' into termial') you can go to the browser and write inton the url:

`http://localhost:3000`

And 'voilà'. you have the page index.pug as you create it.

---------------------

# How to create a express project step by step

Lets replicate [this bootstrap templete](https://blackrockdigital.github.io/startbootstrap-agency/) with the squeleton we just created.
**Credits of the template:**
Copyright 2013-2016 Blackrock Digital LLC.
`git clone https://github.com/BlackrockDigital/startbootstrap-agency.git`

![image 1](/screenshots/1.png)
![image 2](/screenshots/2.png)
![image 3](/screenshots/3.png)
![image 4](/screenshots/4.png)
![image 5](/screenshots/5.png)






