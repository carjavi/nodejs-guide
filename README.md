<p align="center"><img src="https://raw.githubusercontent.com/carjavi/nodejs-guide/master/img/nodejs.png" height="300" alt=" " /></p>
<br>
<h1 align="center">NodeJS Guide</h1> 
<h4 align="right">Oct 22</h4>
<img src="https://img.shields.io/badge/OS-Linux%20GNU-yellowgreen">
<img src="https://img.shields.io/badge/OS-Windows%2011-blue">

<br>

Nodejs delega funciones a los modulos mientras continua el algoritmo, por eso es asincrono.

<br>

# Clone and run repository Github 

To clone and run this repository you'll need [Git](https://git-scm.com) and [Node.js](https://nodejs.org/en/download/) (which comes with [npm](http://npmjs.com)) installed on your computer.

Make sure you have met the requirements listed here: https://docs.nodegui.org/docs/guides/getting-started#developer-environment

From your command line:

```bash
# Clone this repository
git clone https://github.com/nodegui/nodegui-starter
# Go into the repository
cd nodegui-starter
# Install dependencies
npm install
# Run the app
npm start
```

# Modulos
Summary
```
const os = require('os');  // modulo del sistema, no requiere instalación.
const Network = require('./network.js'); // parte del codigo 
console.log('module-name'); // desde donde estas llamando el modulo, se ver el objeto con sus propiedades que son los metodos
module.export = Obj;  //permite exportar un objeto, propiedades, funciones , variables
export.<nombre> = nombre;  // solo permite exportar propiedades que son funciones
```


### Sample 1
exportando metodos desde un objeto. ```index.js```: 
```
const test = requiere('./test.js');
console.log(test.x(a,b));
console.log(test.y(a,b));
```

test.js (modulo)
```
Obj = {};

function x(x1,x2){}
function y(x1,x2){}

// agregamos las propiedades al objeto
module.x = x;
module.y = y;

//exportamos el objeto, funciones , variables
module.exports = Obj;
```

nota: ***module.exports*** tambien puede exportar una fución simplemente
```module.exports = <fuction-name>;```

<br>

---

<br>

### sample 2
exportando propiedades (cada propiedad es una función)
```
index.js (lo que corremos)
const test = requiere('./test.js');
console.log(test.x(a,b));
console.log(test.y(a,b));


test.js (modulo)
function x(x1,x2){}
function y(x1,x2){}

exports.x = x;
exports.y = y;
```
<br>

# funciones Asincronicas y Sincronicas o bloqueante

## sample asincronico
no espera que se ejecute el codigo para continuar
```
const fs = require('fs');

fs.writeFile('./test.text', 'linea1', fuction (err){
    if (err){
        console.log(err);
    }
    console.log("archivo creado");
})
```

```
query('Select * FROM users', function(err, users){
    if (err){
        console.log(err);
    }
    if(users){

    }
});
```


## codigo bloqueante 
espera que se ejecute el cosido para continuar.
```
const result = fs.writeFile('./test.text', 'linea1');
```

```
const users = query('SELECT * FROM Users'); 
```

# Función flecha
```
//To get a default set of Bindings and Parsers
const { SerialPort } = require('serialport')

serialport.close(callback?: error => {}): void
```

<!--  
# asycronomo funtions

# eventos
-->

<br>

---
Copyright &copy; 2022 [carjavi](https://github.com/carjavi). <br>
```www.instintodigital.net``` <br>
carjavi@hotmail.com <br>
<p align="center">
    <a href="https://instintodigital.net/" target="_blank"><img src="https://raw.githubusercontent.com/carjavi/nodejs-guide/master/img/developer.png" height="100" alt="www.instintodigital.net"></a>
</p>



