# JavaScript DOM Manipulation

## Description

This project focuses on practicing **JavaScript** for manipulating the **DOM (Document Object Model)**. You will learn how to interact with HTML elements dynamically through scripts — changing styles, updating content, handling events, and making network requests.

This project is part of the **Holberton School curriculum** and was manually reviewed by peers to ensure code quality and understanding.

---

## Learning Objectives

By the end of this project, you will be able to:

- Select HTML elements using JavaScript
- Understand the differences between ID, class, and tag name selectors
- Modify an element’s style and content
- Dynamically update the DOM
- Use `XMLHttpRequest` and `Fetch API` to make network requests
- Listen and respond to DOM and user events

---

## Requirements

- Use `document.querySelector` and other DOM methods appropriately
- Do not use `var` — only `const` and `let` are allowed
- HTML should not reload on each action — all updates should be made via JavaScript DOM manipulation
- Your scripts must be semi-standard compliant
- JavaScript must be tested on Chrome browser (version 57.0+)
- Each script should be linked to an HTML file for testing

---

## Tasks

### 0. Color Me

**File:** `0-script.js`  
Changes the text color of the `<header>` element to red.

---

### 1. Click and Turn Red

**File:** `1-script.js`  
Changes the text color of the `<header>` to red when the element with id `red_header` is clicked.

---

### 2. Add `.red` Class

**File:** `2-script.js`  
Adds the class `red` to the `<header>` when the `#red_header` is clicked.

---

### 3. Toggle Classes

**File:** `3-script.js`  
Toggles between `red` and `green` classes for the `<header>` when the element with id `toggle_header` is clicked.

---

### 4. List of Elements

**File:** `4-script.js`  
Adds a new `<li>Item</li>` to the `<ul class="my_list">` every time the `#add_item` is clicked.

---

### 5. Change the Text

**File:** `5-script.js`  
Changes the text of the `<header>` to **New Header!!!** when the `#update_header` is clicked.

---

### 6. Star Wars Character

**File:** `6-script.js`  
Fetches the name of a Star Wars character from `https://swapi-api.hbtn.io/api/people/5/?format=json` and displays it inside the element with id `character`.

---

### 7. Star Wars Movies

**File:** `7-script.js`  
Fetches all Star Wars movie titles from `https://swapi-api.hbtn.io/api/films/?format=json` and adds them as `<li>` elements inside the `<ul id="list_movies">`.

---

### 8. Say Hello!

**File:** `8-script.js`  
Fetches a translation of “Hello” from `https://hellosalut.stefanbohacek.dev/?lang=fr` and displays it inside the element with id `hello`. The script is loaded in the `<head>` of the HTML.

---

## Author

👤 **Derick Quiñones**

Project completed as part of Holberton School Higher-Level Programming curriculum.
