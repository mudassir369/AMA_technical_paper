
## 1. let, var, and const

### var
- Function-scoped
- Can be redeclared and updated
```js
var a = 10;
var a = 20;
```

### let
- Block-scoped
- Cannot be redeclared but can be updated
```js
let a = 10;
a = 20;
```

### const
- Block-scoped
- Cannot be redeclared or updated
```js
const a = 10;
// a = 20
```

---

## 2. String Methods
```js
let str = "Hello World";

str.length
str.toUpperCase()
str.toLowerCase()
str.includes("World")
str.slice(0, 5)
str.replace("World", "JS")
```

---

## 3. Creating HTML Elements using JavaScript
```js
const div = document.createElement("div");
div.innerText = "Hello World";
div.style.color = "blue";

document.body.appendChild(div);
```

---

## 4. Difference between forEach() and map()

| Feature     | forEach() | map() |
|------------|----------|-------|
| Return value |  No return |  Returns new array |
| Use case | Iteration | Transformation |

```js
let arr = [1,2,3];

arr.forEach(x => console.log(x));
let newArr = arr.map(x => x * 2);
```

---

## 5. CSS Selectors
```css
p { color: red; }
#id { color: blue; }
.class { color: green; }

div p { }
div > p { }
a:hover { }
```

---

## 6. Array Destructuring
```js
let arr = [10, 20, 30];
let [a, b, c] = arr;
```

---

## 7. bind() Method
```js
const obj = { name: "Mudassir" };

function greet() {
  console.log(this.name);
}

const newFunc = greet.bind(obj);
newFunc();
```

---

## 8. Stack vs Heap Memory
- Stack: primitive values, fast
- Heap: objects, dynamic

```js
let a = 10;
let obj = { name: "JS" };
```

---

## 9. Short Circuit
```js
let result = 0 || "Hello";
let result2 = "Hi" && "World";
```

---

## 10. = vs == vs ===
```js
let a = "5"; //assignment operator
5 == "5" // True
5 === "5" // False
```

---

## 11. Fetch API
```js
fetch("https://api.example.com/data")
  .then(res => res.json())
  .then(data => console.log(data))
  .catch(err => console.log(err));
```

---

## 12. this in method vs function
```js
const obj = {
  name: "JS",
  greet() {
    console.log(this.name);
  }
};
obj.greet();

function test() {
  console.log(this);
}
test();
```

---

## 13. Promises
```js
const promise = new Promise((resolve, reject) => {
  let success = true;

  if (success) resolve("Done");
  else reject("Error");
});
```

---

## 14. Promise.all()
```js
Promise.all([
  Promise.resolve(1),
  Promise.resolve(2)
]).then(res => console.log(res));
```

---

## 15. Promise.any()
```js
Promise.any([
  Promise.reject("Error"),
  Promise.resolve("Success")
]).then(res => console.log(res));
```
