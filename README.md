#📘 YAML Basics – Complete Guide with Examples

This repository contains a comprehensive collection of **YAML examples**, ranging from basic key–value pairs to advanced features used in **Docker Compose**, **Kubernetes**, and **GitHub Actions**.
It is designed for beginners and intermediate learners who want a clear, practical reference for YAML syntax.

---

## ✅ What is YAML?

**YAML (YAML Ain’t Markup Language)** is a human-friendly data serialization format commonly used for:

* Configuration files
* CI/CD pipelines
* Docker Compose
* Kubernetes manifests
* Application settings

YAML uses **indentation with spaces only** (no tabs).

---

# 📚 YAML Examples

Below are all the YAML examples included in this repository.

---

## 🔹 Basic Key–Value Pairs

```yaml
name: Rashedul
country: Bangladesh
age: 22
```

---

## 🔹 YAML Uses Spaces Only (No Tabs)

```yaml
user:
  name: Rashed
  age: 22
```

---

## 🔹 List of Items

```yaml
languages:
  - Python
  - Java
  - Go
```

---

## 🔹 List of Objects

```yaml
users:
  - name: Adam
    age: 22
  - name: Sara
    age: 19
```

---

## 🔹 Nested Objects (Maps)

```yaml
server:
  host: localhost
  port: 8000
  ssl:
    enabled: true
    certificate: "/etc/ssl/cert.pem"
```

---

## 🔹 Multiline Strings

### Literal (preserves formatting)

```yaml
bio: |
  I am a developer.
  I love coding.
```

### Folded (newlines become spaces)

```yaml
description: >
  This text
  will become
  a single line.
```

---

## 🔹 Booleans, Null, Comments

```yaml
is_active: true
nickname: null

nm: Rashed # inline comment
```

---

## 🔹 Anchors & References (Default Values)

```yaml
defaults: &defaultUser
  role: user
  active: true

admin:
  <<: *defaultUser
  role: admin
```

---

# 🐳 Docker Compose Example

```yaml
version: "3.9"

services:
  web:
    image: nginx
    ports:
      - "8080:80"

  db:
    image: postgres
    environment:
      POSTGRES_PASSWORD: secret
```

---

# ☸️ Kubernetes Deployment Example

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: my-app
spec:
  replicas: 2
  selector:
    matchLabels:
      app: demo
  template:
    metadata:
      labels:
        app: demo
    spec:
      containers:
        - name: app
          image: nginx
```

---

# 🛠️ GitHub Action Example

```yaml
name: CI Pipeline

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Install packages
        run: npm install
```

---

# 🍵 "Chai aur Code" YAML Examples

### Inline Comments

```yaml
chai_type: Masala_chai
temperature: hot
savings: 2
browing_time: 5
```

### Nested Recipes

```yaml
chai_recipe:
   base: black_tea
   milk: whole_milk

chai_recipe_two:
   base: black_tea
   milk: whole_milk
```

---

## 🔹 Data Types

```yaml
chai_name: Masala_chai
tagline: 'The best chai in town'
```

---

## 🔹 Incorrect (but useful learning example)

(YAML requires lists under `-` but you wrote simple lines—kept for understanding.)

```yaml
brewing_instruction:
  boil water
  add tea leaves
  add milk
```

Correct way would be:

```yaml
brewing_instruction:
  - boil water
  - add tea leaves
  - add milk
```

---

## 🔹 Numbers & Booleans

```yaml
cups_per_day: 3
cups_per_day_two: 0xFF22FF

is_hot: true
add_sugar: true
add_salt: no
instant: no
```

---

## 🔹 Null

```yaml
sweetner: null
alternatives: ~
```

---

## 🔹 Timestamps

```yaml
morning: 2025-11-26
local: 2025-11-26 08:30:10
```

---

## 🔹 List with Mixed Types

```yaml
spices:
 - ginger
 - cloves
 - black_pepper
 - true
```

---

## 🔹 Nested Lists

```yaml
chai_categories:
 - name: Traditional
   varities:
    - Masala_chai
    - Ginger_chai
    - Cardmon_chai

 - name: Modern
   varities:
    - Vanilla chai
    - Chocolate chai
```

---

## 🔹 Complex Object Example

```yaml
Masala_chai:
  ingredients:
    tea: black_tea
    liquid:
      water: 200ml
      milk: 100ml
    spices:
      ginger: 1_inch
      cinnamon: 1_stick
  preparation:
    tool: small pot
    duration: 5_minutes
```

---

## 🔹 List of Dictionaries

```yaml
Car:
-  name: Honda
   price: 100000
   color: Yellow

-  name: Lambo
   price: 1000000
   color: Yellow
```

---

## 🔹 Anchors for Drinks

```yaml
defaul_chai: &default_base
  tea: black_tea
  water: 200ml
  blewing_time: 5

morning_chai:
  <<: *default_base
  milk: 100ml

evening_chai:
  <<: *default_base
  milk: 150ml

night_chai:
  <<: *default_base
  milk: 200ml
```

---

## 🔹 YAML Tags (Type Casting)

```yaml
zip_code: !!str 12345
count: !!int "123"

unique_spices: !!set
  ? cardamon
  ? ginger
  ? cloves
```

---

# 🎉 Conclusion
