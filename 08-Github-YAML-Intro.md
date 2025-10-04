# What is YAML?

**YAML** = **Y**et **A**nother **M**arkup **L**anguage
(or officially, “YAML Ain’t Markup Language”).

It’s a **human-readable** way to define data — simpler than JSON or XML.
Used for **configuration files** like `workflow.yml`, `docker-compose.yml`, etc.

---

## Basic Syntax Rules

### 1. **Key–Value Pairs**

Just like a dictionary in Python or an object in JSON.

```yaml
name: Suraj
language: English
age: 21
```

Each line defines a **key** followed by a **colon** and its **value**.

---

### 2. **Indentation (VERY IMPORTANT)**

Indentation uses **spaces** (NOT tabs).
Indentation defines **hierarchy (nesting)**.

```yaml
person:
  name: Suraj
  age: 21
  city: Mysuru
```

Here:

* `person` is an object
* `name`, `age`, `city` are inside that object

---

### 3. **Lists (Arrays)**

Lists are created using a **dash (-)** in front of each item.

```yaml
fruits:
  - apple
  - banana
  - mango
```

Equivalent JSON:

```json
{ "fruits": ["apple", "banana", "mango"] }
```

---

### 4. **Nested Lists and Objects**

You can combine both for complex data.

```yaml
students:
  - name: Suraj
    grade: A
  - name: Preetham
    grade: B
```

---

### 5. **Comments**

Use `#` for comments (just like Python).

```yaml
# This is a comment
name: Suraj  # Inline comment
```

---

### 6. **Strings and Quotes**

Usually, quotes are optional — but you can use them when needed.

```yaml
message: "Hello, world!"
title: 'YAML Basics'
note: This works fine too
```

---

### 7. **Booleans, Numbers, Nulls**

```yaml
isActive: true
count: 5
price: 49.99
description: null
```

---

### 8. **Multi-line Strings**

For long text or paragraphs:

```yaml
description: |
  This is a long
  multi-line text.
  It keeps newlines.

summary: >
  This is also a long text
  but newlines are replaced with spaces.
```

---

### Example: GitHub Action (explained)

```yaml
name: My Workflow           # Workflow name
on: push                    # Triggered when code is pushed
jobs:
  greet:
    runs-on: ubuntu-latest  # Runner machine
    steps:
      - name: Print message
        run: echo "Hello, Suraj!"
```

---

**In short:**

* Use **spaces**, not tabs.
* **Indentation = structure**.
* `-` means **list item**.
* `:` separates **key** and **value**.
* `#` adds **comments**.

---