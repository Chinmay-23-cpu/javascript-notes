# Destructuring & Spread Operator

> 📚 Chapter 3 of Objects

---

## 📖 Imagine This...

Suppose someone gives you a bag containing:

- Laptop
- Mouse
- Charger

You don't always need everything.

Sometimes you just want the laptop.

Destructuring lets you take only what you need.

---

# 🤔 What is Destructuring?

Destructuring is a simple way to extract values from an object.

Instead of writing

```javascript
const user = {
    name: "Chinmay",
    age: 20
};

const name = user.name;
const age = user.age;
```

we can write

```javascript
const user = {
    name: "Chinmay",
    age: 20
};

const { name, age } = user;

console.log(name);
console.log(age);
```

### Output

```text
Chinmay
20
```

Much cleaner.

---

# 💻 Renaming Variables

You can give extracted values a different name.

```javascript
const user = {
    name: "Chinmay"
};

const { name: userName } = user;

console.log(userName);
```

### Output

```text
Chinmay
```

---

# 💻 Default Values

If a property doesn't exist,

you can provide a default value.

```javascript
const user = {
    name: "Chinmay"
};

const { city = "Davangere" } = user;

console.log(city);
```

### Output

```text
Davangere
```

---

# 🤔 What is the Spread Operator?

The spread operator (`...`) expands an object or array.

It's commonly used to copy or merge data.

---

# 💻 Copying an Object

```javascript
const user = {
    name: "Chinmay",
    age: 20
};

const copy = { ...user };

console.log(copy);
```

Now `copy` is a new object.

---

# 💻 Merging Objects

```javascript
const user = {
    name: "Chinmay"
};

const details = {
    age: 20
};

const student = {
    ...user,
    ...details
};

console.log(student);
```

### Output

```text
{
  name: "Chinmay",
  age: 20
}
```

---

# 🌍 Where is it Used?

You'll use these features constantly for:

- React props
- Updating objects
- Copying arrays
- API responses
- Cleaner code

---

# ⚠️ Common Mistakes

### ❌ Wrong Destructuring Syntax

Wrong

```javascript
const name = { user };
```

Correct

```javascript
const { name } = user;
```

---

### ❌ Thinking Spread Deep Copies

```javascript
const copy = { ...user };
```

This creates a **shallow copy**, not a deep copy.

---

# 📝 Quick Revision

- Destructuring extracts values from objects.
- Use `{}` while destructuring objects.
- You can rename variables.
- You can provide default values.
- `...` copies or merges objects.

---

# 💻 Mini Exercise

Predict the output.

```javascript
const student = {
    name: "Alex",
    age: 21
};

const { name } = student;

console.log(name);
```

---

Merge these two objects.

```javascript
const a = {
    x: 1
};

const b = {
    y: 2
};
```

---

# 📌 Key Takeaways

- Destructuring makes extracting object properties easier.
- The spread operator copies and merges objects.
- Default values help when a property is missing.
- Both features are heavily used in modern JavaScript.

---

⬅️ Previous: `02-Object-Reference-and-this.md`

➡️ Next: `07-Arrays/01-Arrays.md`