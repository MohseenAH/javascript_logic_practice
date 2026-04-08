# 🧠 FINAL CONCEPT: SHALLOW vs DEEP COPY 🔥

This is just an **extension of what you learned**

---

## 🔹 1. Shallow Copy (You already know this)

👉 Copies only **top level**

```js
let user = {
  name: "Aman",
  address: { city: "Pune" }
};

let copy = { ...user };

copy.address.city = "Mumbai";

console.log(user.address.city); // Mumbai ❌
```

### 👉 Why?

* `address` is still **same reference**

---

## 🔹 2. Deep Copy (Full independent copy)

👉 Copies **everything (including nested)**

```js
let user = {
  name: "Aman",
  address: { city: "Pune" }
};

let copy = JSON.parse(JSON.stringify(user));

copy.address.city = "Mumbai";

console.log(user.address.city); // Pune ✅
```

---

## 🔥 DIFFERENCE TABLE

| Feature            | Shallow Copy | Deep Copy |
| ------------------ | ------------ | --------- |
| Top level          | ✅ copied     | ✅ copied  |
| Nested objects     | ❌ shared     | ✅ copied  |
| Safe from mutation | ❌            | ✅         |

---

## ⚠️ REAL WORLD USE (VERY IMPORTANT)

### ❌ Bug (React / apps)

```js
user.address.city = "Mumbai"; // mutation ❌
```

---

### ✅ Correct

```js
setUser({
  ...user,
  address: { ...user.address, city: "Mumbai" }
});
```

---

