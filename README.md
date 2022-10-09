<p align="center"><img src="https://raw.githubusercontent.com/carjavi/nodejs-guide/master/img/nodejs.png" height="100" alt=" " /></p>
<br>
<h1 align="center">NodeJS Guide</h1> 
<h4 align="right">Oct 22</h4>
<img src="https://img.shields.io/badge/OS-Linux%20GNU-yellowgreen">
<img src="https://img.shields.io/badge/OS-Windows%2011-blue">

<br>

## Modulos
```
const os = requiere(os);  // modulo del sistema
const Network = requiere(./network.js); // parte del codigo 
console.log(module); // desde donde estas llamando el modulo, se ver el objeto con sus propiedades que son los metodos
```


### Sample 1
exportando metodos desde un objeto. ```index.js```: 
```
const test = requiere(./test.js);
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

nota: module.exports tambien puede exportar una fucnion simplemente
```module.exports = <name fuction>;```



---


### sample 2
exportando propiedades
```
index.js (lo que corremos)
const test = requiere(./test.js);
console.log(test.x(a,b));
console.log(test.y(a,b));


test.js (modulo)
function x(x1,x2){}
function y(x1,x2){}

exports.x = x;
exports.y = y;
```



---
// To get a default set of Bindings and Parsers
const { SerialPort } = require('serialport')

serialport.close(callback?: error => {}): void

asycronomo funtions

eventos

---
Copyright &copy; 2022 [carjavi](https://github.com/carjavi). <br>
```www.instintodigital.net``` <br>
carjavi@hotmail.com <br>
<p align="center">
    <a href="https://instintodigital.net/" target="_blank"><img src="https://raw.githubusercontent.com/carjavi/nodejs-guide/master/img/developer.png" height="100" alt="www.instintodigital.net"></a>
</p>



