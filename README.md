# JavaScript Cheat Sheet

## From the Author:

This beautiful notes was made by Wreaking#9752. Join my Discord Server: https://discord.gg/Z7JXdVbE2J

- I made these notes, because I usually forget some stuff about JavaScript. So I used to refer from these notes.
- I thought of sharing these notes with everyone, because everyone deservers to learn JavaScript.
- I tried my best to make it easy for you guys, so that you understand the basic concept.
- You need to practice it on a daily basis, if you are willing to learn JavaScript.
- I recommend you to use https://replit.com and select node.js or JavaScript.

## Introduction:

First of all you need to be good at Algebra and basic Mathematics, and if you're not, make sure to brush up those concepts.

So, let's begin!

```
console.log("Welcome to JavaScript!")
```
## Declaration & It's Uses:

***

Declaring variables in JS are,
- `const`,
- `var`,
- `let`

`var` was the most commonly used declaring variable in older days, but now-a-days, `const` and `let` are mostly used.

There are differences in using these 3 declaring variable, here's a simple table that explains it all,

| Declaring Variable | Block Scoped     | Creates Global Property   | Re-assignable         |  Re-declarable    |
| :---:              | :---:            |    :---:                 |          :---:        |         :---:     |
| `var`              | ❌               | ✔                        | ✔                     | ✔                |
| `let`              | ✔                | ❌                       | ✔                     | ❌               |
| `const`            | ✔                | ❌                       | ❌                    |❌                |

From the table, we can conclude that, if a variable is decalred using `var` or `let`, we can assign a new value to that same varible, even though an older value is assigned to it. For an example,

```js
let a = 5
let b = 6
a = b + a

console.log(a)
```

Here, `a` will return the new value, although if it was delacred using `const`, it will not work anymore.

`Note:` Recently, JavaScript released two important keywords `let` and `const`. These two keywords provide Block Scope in JavaScript. Variables declared inside a `{}` block cannot be accessed from outside the block. For example,

```js
{
  let x = 2;
}
```

Here, `x` cannot be used out of the block. But we can use `var` inside and outside the block,

```js
{
  var x = 2;
}
```

In this case, `x` can be used outside the block, because `var` doesn't have `Blocked Scope` property.

## Variables:

Variables are used to store temporary data. For an example,

```js
var x = 5
var y = 6
```

In this example `x` and `y` both are variable, with the value of 5 and 6 stored in it respectively.
  we can use const and let instead of var.

In JavaScript, if you declare a variable without any of `let`, `const` or `var`, by default, it registers the variable as `let`. For example,
```js
x = 5
y = 10
z = a + b

console.log(z) // Value of z will be 15
```

## Data Types:

The set of types in the JavaScript language consists of `Primitive Values` and `Objects`.

- Primitive Values
    - Boolean
    - Null
    - Undefined
    - Number
    - BigInt
    - String
    - Symbol
- Objects (Collector of Properties)

Get a detailed infomration at [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures).

> Difference between `"="` and `"=="`
> - `"="`: This is assigment operator
> - `"=="`: This is equal to operator<br>
>
> So, you can save a value to a variable by using, `"="` and check whether the value of the variable is equal to another value by using `"=="`.

> Declaring variables in one line
> - Use comma to seperate it,
> ```js
> let x = "Among us", y = "is sus", z = 100
> ```
> Or you can do this different lines,
> ```js
> let x = 'Among us';
> let y = 'is sus';
> let z = 100;
> ```
> You can also, declare `undefined` variables first, and then save data to them.<br><br>
> `Note:` Semi-colon (`;`) is used to finish a line. Although, the current versions of JS doesn't require "`;`" at end of the line.

> We can add `Strings`, `Numbers`, `Booleans` like,
> ```js
> let x = "abcc" // <- is a string
> let y = 100 // <- is a number
> let z = true or false // <- is a boolean
> ```
> If you don't assign any value to a variable, JS will register the value as `undefined`. Remember, a `String` is always defined inside `""` or `''`.

## Try It Yourself:

Log the values of these given problems.

```js
let x = 5 + 4 + 7
console.log(x)
```
```js
let k = "10" + 4 + 4
console.log(k)
```
```js
let y = "FBI" + " " + "OPEN" + " " + "UP"
console.log(y) 
```

## Explanation:

```js
const x = 5
```

> In this code, `const` is a declaration. `x` is the a defined as a variable. `=` is assignment 

## Operators:


> Operators are defined as the basic Mathematical addition, subraction, multiplication and more, `+`, `-`, `*`, `/`.

For example,

```js
(2 + 2) * 10
```

## Expression:

> Expression is a combination of values, variables, and operators, which computes (to calculate an answer or amount by using a machine) to a value.

For example,
```js
10 * 10 // evalutes 100
```

```js
let x = 5
let z = x * 5

console.log(z)
```
> The answer will be `25`. We will learn about console logs later.

```js
"Wrea" + "" + "king" // It evaluates (to determine or fix the value of) as "Wreaking"
```
```js
"Wrea" + " " + "king" // It evaluates as "Wrea king", because we have added a space between the quotes (string).
```

## Comments:

> `//` -> Two forward slashes place one after another are known as a comment. It can be used to explain a particular statement or a bunch of statement. Texts written inside it are ignored by JS hence, they cannot be executed.

For example,

```js
let y = 10
// let x = 8 -> This line will be ignored while execution of the code
```

> `/*  */` -> We can use this to comment out a portion of a code. Code, inside this slashes, won't get executed.

For example,
```js
/*
let x = "wow"
let z = "among"
let y = "sus" -> These three lines of codes will be ignored and won't be executed
*/
```

## Identifiers:

> JavaScript Identifiers are named as variables, functions, etc.

> **Caution:**<br>
> - You cannot use JS reserved keywords as the name of a variable. Such as, `break`, `new` or `boolean` variable names are not a valid variable name.
> - Variable names cannot contain any special or numeric characters. The only excepted speical characters are `-` & `_`.

We can use two variables to define two strings like,
```js
let title, surname

title = "Wrea"
surname = "king"

console.log(title) // Result will be "Wrea"
console.log(surname) // Result will be "king"
```
> `Note:` Before assigning the two variables to their values, if we console logged the two variables, we'd get `undefined`.

## Camel Case:

> **What is it?**<br>
When multiple words are used to form a variable, `camel case` joins those words together, without any white space, and delineates (to describe) the start of each new word with a capital letter.

Camel Case are of 2 types,
- `Upper Camel Case (Pascal Case):`
FirstName, LastName, MasterCard, InterCity.
- `Lower Camel Case:`
firstName, lastName, masterCard, interCity.

# Credits

`Written by:` [Wreaking#9752]() ([Discord Server](https://discord.gg/Z7JXdVbE2J))<br>
`Edited & Updated by:` [DragoLuca#3636](https://github.com/dragoluca22) ([Discord Server](https://dsc.gg/dragoluca))

# References
- [w3Schools](https://www.w3schools.com/)
- [MDN Web Docs](https://developer.mozilla.org/en-US/)

# 🔗 Links
[![Discord](https://img.shields.io/badge/Discord-%237289DA.svg?logo=discord&logoColor=white)](https://dsc.gg/dragoluca) [![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?logo=Instagram&logoColor=white)](https://instagram.com/sarthakkundu22) [![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/sarthak-kundu-608479220) [![Stack Overflow](https://img.shields.io/badge/-Stackoverflow-FE7A16?logo=stack-overflow&logoColor=white)](https://stackoverflow.com/users/16536353) [![Twitter](https://img.shields.io/badge/Twitter-%231DA1F2.svg?logo=Twitter&logoColor=white)](https://twitter.com/skk_at) [![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?logo=YouTube&logoColor=white)](https://youtube.com/c/UCFTLRtd7NMfdD_R8ftqXBzQ) 
