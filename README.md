# Variables, Scope and Memory



## prmitive and reference values

ECMAScript variables contain 2 deffrent types of data: **primitive** values and **reference** values.

1. **primitive** values => accessed by value;
2. **reference** values => accessed by reference.

### Dynamic Properties

1. **primitive** values can't have properties added to them even though attempting to do so won't cause an error:

   ```js
   let name = "evan"
   name.age = 29
   console.log(name.age) // undefined
   ```

2. **reference** values can have properties added and assigned.

### Copying Values / Argument Passing

Always **Pass by values**. For primitive values, it passes the real value; for reference values, it means the reference.

```js
// copying values
let objA = { name: 'tim' }
let objB = objA  // passing the reference to objB
objB.name = 'cook'
console.log(objA)  // { name: 'cook'}
objB = {} 
console.log(objA)  // { name: 'cook' }

// argument passing
const test = obj => {
  obj.age = 21
  obj = {}
}

let obj1 = { name: 'bryan' }
test(obj1)
console.log(obj1) // { name: 'bryan', age: 21 }
```

### Determining Type

Two ways to check a varible's type: `typeof` and `instanceof`

```js
// syntax
typeof variables // returns the specific 
variables instanceof constructor
```

### Execution Context And Scope

The **execution context** of a variable or function defines what other data it has access to, as well as how it should behave.

