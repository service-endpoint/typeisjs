<p align="center"><a href="https://typeis.github.io/" target="_blank"><img width="200"src="https://typeis.github.io/typeis.png"></a></p>

In Javascript, "Everything is (or acts like) an Object"
We need to write "typeis.js" due to a problem (type check) arised other than except the conveniences it is a providing to us.

#typeis.js
###Typeis. it's the smart and simple javascript type check and validation library ~226 Bytes;

|Value                  |Native     |Typeis.js  |
|---                    |---        |---        |
|Undeclared variables   |undefined  |---        |
|undefined              |undefined  |---        |
|null                   |object     |---        |
|Booleans               |boolean    |Boolean    |
|Numbers                |number     |Number     |
|String                 |string     |String     |
|Functions              |function   |Function   |
|Array                  |object     |Array      |
|Object                 |object     |Object     |
|Date                   |object     |Date       |
|RegExp                 |object     |RegExp     |
####Be careful!
Everything in JavaScript acts like an object, with the only two exceptions being **null** and **undefined**. *[JavaScript Garden](https://bonsaiden.github.io/JavaScript-Garden/#object.general)
Typeis.js acts like an property; doesn't work null and undefined types because they doesn't have properties.

###Download

* [typeis.js ~813 B (413 B gzipped)](https://raw.githubusercontent.com/typeis/typeisjs/master/typeis.js)
* [typeis.min.js ~305 B (226 B gzipped)](https://raw.githubusercontent.com/typeis/typeisjs/master/dist/typeis.min.js)

###installation
```javascript
npm install typeis
bower install typeis
```
###usage
In Node.js:
```javascript
require('typeis');
```
In a browser:
```html
<script src="typeis.js"></script>
```
####examples
Basic type checking
```javascript
variable.typeis();
// return Array, Object, RegExp, Date etc.
```
Multi type validation
```javascript
variable.typeis(['array', 'object']);
// if variable is Array or Object return true otherwise false
```
Type valition with regex
```javascript
variable.typeis('array|object');
// if variable is Array or object return true otherwise false

variable.typeis('.+[yep]$');
// if variable type end of "y", "e" and "p" like Array, Date, RegExp return true otherwise false

variable.typeis('(^(?!array|object).+)[^n]$');
// if variable is Array, Object or ending "n" like Function and Boolean return false otherwise true
```

####Real world Usage

```javascript 
function realWorld( options ){
    if(options.typeis('object')){
        //do something
    } else {
        //do another something
    }
}
```

####Browser Support
IE9 and below also support all modern browser.

####Changelog
#####1.0.x
Typeis.js Released

#####1.1.x
Multi type validation support
```javascript
variable.typeis(['array', 'object']);
// if variable is Array or Object return true otherwise false
```
type validation with regex support
```javascript
variable.typeis('array|object');
// if variable is Array or object return true otherwise false
```
