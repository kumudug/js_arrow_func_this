# js_arrow_func_this
## Arrow functions and this.

### __Normal Function__
```javascript
const person = {
    name: "kumudu",
    greet: function() {
        console.log(this.name);
    }
}

person.greet();
```
*Output*
```
kumudu
```

### __Arrow Function__
```javascript
const person = {
    name: "kumudu",
    greet: () => console.log(this.name)
}

person.greet();
```
*Output*
```
undefined
```

__*This is because in arrow functions this is refering to global scope*__

### __Arrow Function (Working)__
```javascript
const person = {
    name: "kumudu",
    greet() {
        console.log(this.name);
    } 
}

person.greet();
```
*Output*
```
kumudu
```
