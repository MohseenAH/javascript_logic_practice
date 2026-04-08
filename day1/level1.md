Perfect —  ***Level 1***  **ultimate Level 1 revision sheet (with examples)** 💯


---

# 🧠 1. Primitive vs Non-Primitive

### ✅ Primitive

```js
let a = 10;
let b = "hello";
let c = true;
```

👉 Simple values (number, string, boolean, null, undefined)

---

### ❌ Non-Primitive

```js
let obj = { name: "Aman" };
let arr = [1, 2, 3];
```

👉 Complex values (objects, arrays, functions)

---

# 🧠 2. Value vs Reference

### ✅ Value (Primitive)

```js
let a = 10;
let b = a;

b = 20;

console.log(a); // 10 ✅
```

---

### ❌ Reference (Object)

```js
let a = { value: 10 };
let b = a;

b.value = 20;

console.log(a.value); // 20 ❌
```

---

# 🧠 3. Memory Behavior

### ✅ Separate Memory (Primitive)

```js
let a = 5;
let b = a;

b = 10;
```

```txt
a → 5
b → 10
```

---

### ❌ Shared Reference (Object)

```js
let a = { x: 1 };
let b = a;

b.x = 2;
```

```txt
a ──▶ { x: 2 }
b ──▶ SAME OBJECT
```

---

# 🧠 4. Spread Operator

### ✅ Works for top-level copy

```js
let user = { name: "Aman" };

let copy = { ...user };

copy.name = "Rahul";

console.log(user.name); // Aman ✅
```

---

# 🧠 5. Shallow Copy

```js
let user = {
  name: "Aman",
  address: { city: "Pune" }
};

let copy = { ...user };

copy.address.city = "Mumbai";

console.log(user.address.city); // Mumbai ❌
```

👉 Nested object still shared

---

# 🧠 6. Deep Copy (Basic Idea)

```js
let user = {
  name: "Aman",
  address: { city: "Pune" }
};

let copy = JSON.parse(JSON.stringify(user));

copy.address.city = "Mumbai";

console.log(user.address.city); // Pune ✅
```

👉 Fully independent copy

---

# 🔥 FINAL ONE-LINE SUMMARY

```txt
Primitive → value copy → separate memory ✅  
Object    → reference → shared memory ❌  
Spread    → shallow copy (1 level only)  
Deep copy → fully independent  
```

---

