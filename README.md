# 🥗 Calorie Counter

A simple, interactive web-based calorie tracking tool that helps users monitor their daily food intake, exercise, and calorie budget in real time.

## 📌 Features

* Set a daily calorie budget
* Log meals under **Breakfast**, **Lunch**, **Dinner**, and **Snacks**
* Log **Exercise** to subtract burned calories from your daily total
* Add multiple entries dynamically under each category
* Calculate remaining calories
* Display calorie **Surplus** or **Deficit**
* Clear all inputs with one click

---

## 🚀 Getting Started

### 📂 Project Structure

```
📁 calorie-counter/
├── index.html        # Main HTML structure
├── styles.css        # Styling with CSS variables
└── script.js         # JavaScript logic for interaction
```

### 💻 How to Use

1. **Open `index.html`** in any modern web browser.
2. **Enter your daily calorie budget.**
3. **Add entries** to each meal or exercise section using the dropdown and "Add Entry" button.
4. **Click "Calculate Remaining Calories"** to see your results.
5. **Clear all fields** by clicking the "Clear" button.

---

## 🧠 Technologies Used

* **HTML5** – Semantic structure
* **CSS3** – Custom properties and layout styling
* **JavaScript (Vanilla)** – DOM manipulation, form handling, and validation

---

## 📄 Code Highlights

### ✅ Input Cleaning & Validation

```js
function cleanInputString(str) {
  const regex = /[+-\s]/g;
  return str.replace(regex, '');
}

function isInvalidInput(str) {
  const regex = /\d+e\d+/i;
  return str.match(regex);
}
```

### 🔄 Dynamic Entry Injection

```js
function addEntry() {
  const targetInputContainer = document.querySelector(`#${entryDropdown.value} .input-container`);
  ...
  targetInputContainer.insertAdjacentHTML('beforeend', HTMLString);
}
```

---

## 📦 Future Improvements

* Save data using **localStorage**
* Add **charts** or **graphs** for visual feedback
* Mobile responsiveness improvements
* Add authentication and persistent tracking

---

## 📃 License

This project is open-source and available under the [MIT License](LICENSE).

---

## ✍️ Author

**Oluwatobiloba Alomaja**
