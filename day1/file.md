Perfect — let’s lock it with **one clear example for each** 👇

---

# 🧠 1. Primitives (Copied by Value)

```js
let a = 10;
let b = a;

b = 20;

console.log(a); // 10 ✅
console.log(b); // 20
```

### 👉 What’s happening:

* `a` and `b` have **separate memory**
* changing `b` does NOT affect `a`

---

# 🧠 2. Objects / Arrays (Copied by Reference)

```js
let a = { value: 10 };
let b = a;

b.value = 20;

console.log(a.value); // 20 ❌
console.log(b.value); // 20
```

### 👉 What’s happening:

* `a` and `b` point to the **same memory**
* changing `b` ALSO changes `a`

---

# 🔥 FINAL UNDERSTANDING

```txt
Primitive → separate memory → safe ✅
Object    → shared memory   → linked ❌
```

---

If this is clear, you’ve fully mastered Level 1 💯
👉 Ready for brain-twisting part? Say **"level 2"** 🔥
