##Jet

A friendlier syntax for writing PHP.

Jet is a small language (a variant of [ES6][1]) that compiles to clean, readable PHP. Jet tries to take the good parts of PHP and expose them with a simple, familiar syntax. This is all while maintaining compatibility with existing PHP code you may have in your application.

Read more: [Why does PHP need Fixing?][2]

###Objectives

 * Remove much of PHP's ugliness without changing the core way the language works 
 * Normalize inconsistencies and nicely organize global functions and core libraries
 * Support Unicode in all string operations
 * Maintain compatibility with existing PHP code as much as possible
 * Enable and encourage good practices like encapsulation and privately scoped variables
 * Discourage bad practices like polluting the global namespace

With Jet, you can do things like:

 * Create lists and sets using simple `[]` and `{}` syntax
 * Write a set of "private" classes and expose/export only a single one
 * Write functional code using closures and privately scoped variables
 * Create a plugin or add-on in Jet for an existing PHP application like WordPress
 * Use Regular Expression literals and unicode strings

###Example

Jet:
```js
class User {
  constructor(name) {
    this.name = name;
  }
  getName() {
    return this.name;
  }
  static create(name) {
    return new User(name);
  }
}

['Alice', 'Bob'].forEach((name) => {
  var user = User.create(name);
  echo(user.getName());
});
```

[1]: https://en.wikipedia.org/wiki/ECMAScript#ECMAScript_Harmony_.286th_Edition.29
[2]: https://github.com/phpjet/phpjet/wiki/Fixing-PHP
