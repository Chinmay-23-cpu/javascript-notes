# Object References, Cloning & this Keyword

> 📚 Chapter 2 of Objects

---

## 📖 Imagine This...

Suppose you give your friend the key to your house.

Both of you now access the **same house**.

If your friend paints the wall,

you'll also see the new color.

Objects work the same way.

Variables store a **reference** to an object, not a copy of it.

---

# 🤔 Object References

Look at this example.

```javascript
const user1 = {
    name: "Chinmay"
};

const user2 = user1;
```

Did we create two objects?

❌ No.

Both variables point to the **same object**.

```text
user1 ───┐
          │
          ▼
      { name: "Chinmay" }
          ▲
          │
user2 ────┘
```

---

# 💻 Example

```javascript
const user1 = {
    name: "Chinmay"
};

const user2 = user1;

user2.name = "Rahul";

console.log(user1.name);
```

### Output

```text
Rahul
```

Why?

Because both variables refer to the same object.

---

# 🤔 How to Clone an Object?

Sometimes we want a completely new object.

The easiest way is using the **spread operator**.

```javascript
const user1 = {
    name: "Chinmay",
    age: 20
};

const user2 = { ...user1 };

user2.name = "Rahul";

console.log(user1.name);
console.log(user2.name);
```

### Output

```text
Chinmay
Rahul
```

Now they are different objects.

---

# 🤔 What is `this`?

`this` refers to **the object that is calling the method**.

Example

```javascript
const student = {

    name: "Chinmay",

    greet() {
        console.log("Hello " + this.name);
    }

};

student.greet();
```

### Output

```text
Hello Chinmay
```

Here,

```javascript
this.name
```

means

```javascript
student.name
```

---

# 💻 Why not just use `name`?

```javascript
const student = {

    name: "Chinmay",

    greet() {
        console.log(name);
    }

};
```

This causes an error because JavaScript looks for a variable named `name`.

Instead,

```javascript
this.name
```

tells JavaScript to use the `name` property of the current object.

---

# 🌍 Real-Life Example

Think of a mobile phone.

```text
Phone

↓

Brand

Model

Battery

Camera
```

If the phone says,

> "My battery is 80%."

The word **my** refers to **that phone**.

Similarly,

`this` means

> "This object."

---

# ⚠️ Common Mistakes

### ❌ Thinking Objects are Copied

```javascript
const a = { x: 1 };

const b = a;
```

This creates a reference, not a copy.

---

### ❌ Forgetting `this`

Wrong

```javascript
console.log(name);
```

Correct

```javascript
console.log(this.name);
```

inside an object method.

---

### ❌ Expecting Spread to Deep Clone

```javascript
const copy = { ...original };
```

This creates a **shallow copy**.

Nested objects are still shared.

We'll learn deep cloning later.

---

# 📝 Quick Revision

- Objects are stored by reference.
- Assigning one object to another copies the reference.
- Use the spread operator to clone an object.
- `this` refers to the object calling the method.
- Spread creates a shallow copy.

---

# 💻 Mini Exercise

Predict the output.

```javascript
const person = {
    name: "Alex"
};

const user = person;

user.name = "Sam";

console.log(person.name);
```

---

Predict the output.

```javascript
const person = {
    name: "Alex",

    greet() {
        console.log(this.name);
    }
};

person.greet();
```

---

# 📌 Key Takeaways

- Objects are assigned by reference.
- Changing one reference changes the same object.
- Use `{ ...object }` to create a new object.
- `this` refers to the current object.
- Spread creates a shallow copy.

---

⬅️ Previous: `01-Objects.md`

➡️ Next: `03-Destructuring-and-Spread.md`