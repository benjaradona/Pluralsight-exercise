#### Javascript Best Practices
### Diverse
- use ";"
- use lint / hint
- 'use strict'
- name callbacks and return (err)
#### ES6 and babel
- let -> var
- 'npm install –g babel-cli'
- create '.babelrc' (JSON-file with presets och plugins)
- 'npm install –save- babel-preset-es2015'
- 'babel app.js –o es6.js'
#### Async/Await eliminates the need for callbacks and promises
- 'async' allows a keyword 'await'. 
See kangax-github.io/compat-table/esnext/ to see which "presets" needs to be put in .babelrc and 
installed. For 'async' the 'stage-3' preset needs to be used. Then
'npm install -save babel-preset-stage-3'

### Production Code
#### npm
The first thing you want to do is
'npm init' -> creates the 'package.json'
##### package.json
"enginges": {    
    "node": "4.2.1"   
} says "This is only for "node 4.2.1"

'npm install express --save' puts express in "dependenices" in package.json that could be breaking
Instead do
'npm config set save-exact=true' -> makes it automatically save it to package.json and dependencies 
are exact versions that you know work.

#### Environment
A number of things will change from one environment to the next.

Use a tool called node foreman: 'npm install -g foreman'

Then you can put 
"script" {
    "start": "node app.js"
    } 
and then run 

nf start your code and automatically set ports etc. Specify them in .env

{
    "port" : 9000,
    "connection":{
        "sql":"",
        "mongo":""
    }    
}

and node foreman will take that and put it in my process when I 'nf start'. Make sure to set you 
environment variables and use them with node foreman.

#### Cross platform
node.js is cross platform. In mac and windows myobject and myObject are the same thing. Not in Linux.
Make every file lowercase or camel-case.

#### Keep it simple
Tools are for solving problems... Not for making them...
Best practices is not the same as toolsets.
    
Skriver bara för att se om git reagerar.
