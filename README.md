# js-bcrypt
bcrypt hashing algorithm for JavaScript in Dojo module

## How to use

If you want to use with Dojo just import the dependency. On VanillaJS just add the script file.

## Dojo Example

```javascript
define([
	"dojo/_base/declare",
    "./Bcrypt"
], function(declare, Bcrypt){
	var example = declare('my.app.example', null, {
		myfunction: function() {
			var bcrypt = new bcrypt();
			console.log(bcrypt.gensalt(10));
		}
	});
}
```

## Vanilla JS Example
```javascript
var bcrypt = new bcrypt();
console.log(bcrypt.gensalt(10));
```
## Exposed methods

### Hashing password
```javascript
var hashed = bcrypt.hashpw(password, salt, callback);
```
### Generating salt
```javascript
var salt = bcrypt.gensalt(log_rounds);
```
### Check password
```javascript
var boolean = bcrypt.checkpw(plaintext, hashed, callback);
```