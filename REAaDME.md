
# Make a Calculator Using HTML CSS And JavaScript

Project description (short)

A clean, responsive calculator built with HTML, CSS, and vanilla JavaScript. It supports the four basic arithmetic operations (add, subtract, multiply, divide), decimals, percentages, parentheses, keyboard input, and includes clear/backspace buttons. The UI is mobile-friendly, accessible (ARIA attributes, keyboard focus), and visually minimalist so it’s easy to style or extend.

Use cases

* Learning DOM manipulation and event handling in JavaScript.

* Embedding in a portfolio or web project.

* Starting point for adding advanced features (history, memory buttons, scientific functions).





## Acknowledgements

 - [Awesome Readme Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
 - [Awesome README](https://github.com/matiassingers/awesome-readme)
 - [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)


## Appendix

This project is a simple yet fully functional calculator built using only HTML, CSS, and JavaScript — no external libraries or frameworks required. It demonstrates how to handle user input, perform basic arithmetic operations, and update the UI dynamically using JavaScript DOM manipulation.

🔍 Project Overview

The calculator performs standard mathematical operations such as:

Addition (+)

Subtraction (−)

Multiplication (×)

Division (÷)

Percentage (%)

Decimal point input (.)

Clear and backspace functionality

The interface is clean, responsive, and easy to use — suitable for both desktop and mobile screens. Users can interact with it using both mouse clicks and keyboard inputs.

🧰 Technologies Used

HTML – Provides the basic structure and layout of the calculator.

CSS – Styles the calculator, making it visually appealing and responsive.

JavaScript – Handles all the logic and calculations, updates the display, and manages events for buttons and keyboard inputs.

⚙️ Key Features

Real-time input and output display

Error handling for invalid expressions

Keyboard support for easier operation

Responsive design for mobile and desktop devices

Smooth button animations and hover effects

Clean and minimal UI design for better user experience

💡 Learning Outcomes

By building this calculator, you’ll learn how to:

Use JavaScript to manipulate the DOM in real time

Handle user interactions using event listeners

Implement arithmetic operations programmatically

Manage state and update the display dynamically

Design responsive layouts using CSS Grid or Flexbox

🚀 Project Improvements (Optional)

You can enhance this project by adding:

Scientific mode (sin, cos, tan, square root, power, etc.)

Calculation history

Dark/Light mode toggle

Memory buttons (M+, M−, MR)

Theme customization


## Features

- Features
* Clickable buttons and keyboard input (digits, + - * / . Enter Backspace).

* Expression evaluation with basic validation and percent handling (50% → 0.5).

* Clear (C) and backspace (←) controls.

* Responsive layout with accessible labels and focus states.

* Error handling for invalid expressions.


## Usage/Examples

```javascript
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Calculator — HTML CSS JS</title>
  <style>
    :root{
      --bg:#0f1724;
      --panel:#111827;
      --accent:#10b981;
      --muted:#9ca3af;
      --btn:#1f2937;
      --shadow: 0 6px 18px rgba(2,6,23,0.6);
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }
    html,body{height:100%;margin:0;background:linear-gradient(180deg,var(--bg),#071021);display:flex;align-items:center;justify-content:center;padding:24px;color:#e6eef8}
    .calculator{
      width:360px;
      max-width:100%;
      background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      border-radius:18px;
      padding:16px;
      box-shadow:var(--shadow);
      box-sizing:border-box;
    }
    .display{
      background:transparent;
      color:#e6eef8;
      min-height:78px;
      display:flex;
      flex-direction:column;
      justify-content:center;
      padding:12px;
      border-radius:12px;
      margin-bottom:12px;
      word-break:break-all;
    }
    .expression{
      font-size:14px;
      color:var(--muted);
      line-height:1;
      max-height:36px;
      overflow:hidden;
    }
    .result{
      font-size:28px;
      font-weight:600;
      margin-top:6px;
    }
    .pad{
      display:grid;
      grid-template-columns: repeat(4, 1fr);
      gap:10px;
    }
    button.btn{
      border:0;
      background:var(--btn);
      color:#e6eef8;
      padding:14px;
      border-radius:10px;
      font-size:18px;
      cursor:pointer;
      box-shadow: 0 2px 6px rgba(2,6,23,0.6);
      transition:transform 0.06s ease, box-shadow 0.06s;
      user-select:none;
    }
    button.btn:active{transform: translateY(1px)}
    button.op{ background: linear-gradient(180deg,#0ea5a0,#059669); font-weight:600; color:white; }
    button.wide{grid-column: span 2}
    button.alt{ background: transparent; border:1px solid rgba(255,255,255,0.05); color:var(--muted); }
    button.btn:focus{outline:3px solid rgba(16,185,129,0.18)}
    @media (max-width:420px){
      .result{ font-size:22px }
      button.btn{ padding:12px; font-size:16px }
    }
  </style>
</head>
<body>
  <main class="calculator" role="application" aria-label="Calculator">
    <div class="display" id="display" aria-live="polite">
      <div id="expression" class="expression" aria-hidden="true"></div>
      <div id="result" class="result" aria-atomic="true">0</div>
    </div>

    <section class="pad" role="group" aria-label="Calculator keypad">
      <button class="btn alt" data-action="clear" aria-label="Clear">C</button>
      <button class="btn alt" data-action="back" aria-label="Backspace">←</button>
      <button class="btn alt" data-value="(" aria-label="Left parenthesis">(</button>
      <button class="btn op" data-value="/" aria-label="Divide">÷</button>

      <button class="btn" data-value="7" aria-label="Seven">7</button>
      <button class="btn" data-value="8" aria-label="Eight">8</button>
      <button class="btn" data-value="9" aria-label="Nine">9</button>
      <button class="btn op" data-value="*" aria-label="Multiply">×</button>

      <button class="btn" data-value="4" aria-label="Four">4</button>
      <button class="btn" data-value="5" aria-label="Five">5</button>
      <button class="btn" data-value="6" aria-label="Six">6</button>
      <button class="btn op" data-value="-" aria-label="Minus">−</button>

      <button class="btn" data-value="1" aria-label="One">1</button>
      <button class="btn" data-value="2" aria-label="Two">2</button>
      <button class="btn" data-value="3" aria-label="Three">3</button>
      <button class="btn op" data-value="+" aria-label="Plus">+</button>

      <button class="btn wide" data-value="0" aria-label="Zero">0</button>
      <button class="btn" data-value="." aria-label="Decimal point">.</button>
      <button class="btn op" data-value="%" aria-label="Percent">%</button>

      <button class="btn op wide" data-action="evaluate" aria-label="Equals">=</button>
    </section>
  </main>

  <script>
    (function(){
      const exprEl = document.getElementById('expression');
      const resEl = document.getElementById('result');
      const allButtons = document.querySelectorAll('button.btn');
      let expression = '';

      function updateView(){
        exprEl.textContent = expression || '';
        resEl.textContent = expression ? tryEvaluatePreview(expression) : '0';
      }

      function tryEvaluatePreview(expr){
        try {
          const val = safeEval(expr);
          if (typeof val === 'number' && isFinite(val)) return String(val);
          return 'Err';
        } catch (e) {
          return '';
        }
      }

      // Basic sanitization and percent handling
      function sanitizeForEval(input){
        // keep only digits, operators, parentheses, decimal, spaces and percent
        const allowed = /^[0-9+\-*/().%\s]+$/;
        if (!allowed.test(input)) throw new Error('Invalid characters');
        // convert occurrences like 50% to (50/100)
        // also handle decimals: 12.5% -> (12.5/100)
        return input.replace(/(\d+(\.\d+)?)%/g, '($1/100)');
      }

      function safeEval(input){
        const sanitized = sanitizeForEval(input);
        // evaluate in function scope (safer than raw eval but still local)
        // Note: For production use, prefer a math parsing library.
        // eslint-disable-next-line no-new-func
        return Function('"use strict"; return (' + sanitized + ')')();
      }

      function appendValue(val){
        // basic rule checks: prevent two operators in a row (except unary minus)
        const lastChar = expression.slice(-1);
        const operators = '+-*/%';
        if (operators.includes(val)){
          if (expression === '' && val !== '-') return; // only allow leading minus
          if (operators.includes(lastChar)) {
            // replace previous operator (unless lastChar is '(')
            if (lastChar === '(' && val !== '-') return;
            expression = expression.slice(0, -1) + val;
            return;
          }
        }

        if (val === '.'){
          // prevent multiple decimals in current number fragment
          const afterSplit = expression.split(/[\+\-\*\/\(\)]/).pop();
          if (afterSplit.includes('.')) return;
        }

        expression += val;
      }

      function handleAction(action){
        if (action === 'clear'){
          expression = '';
        } else if (action === 'back'){
          expression = expression.slice(0, -1);
        } else if (action === 'evaluate'){
          if (!expression) return;
          try {
            const result = safeEval(expression);
            if (!isFinite(result)) throw new Error('Math error');
            expression = String(result);
          } catch (e) {
            expression = '';
            resEl.textContent = 'Error';
            setTimeout(() => { resEl.textContent = '0' }, 700);
          }
        }
      }

      allButtons.forEach(btn => {
        btn.addEventListener('click', () => {
          const val = btn.dataset.value;
          const action = btn.dataset.action;
          if (action) {
            handleAction(action);
          } else if (val !== undefined) {
            appendValue(val);
          }
          updateView();
        });
      });

      // Keyboard support
      window.addEventListener('keydown', (ev) => {
        const k = ev.key;
        if ((/[\d+\-*/().%]/).test(k)) {
          ev.preventDefault();
          appendValue(k === '/' ? '/' : k);
          updateView();
          return;
        }
        if (k === 'Enter' || k === '=') {
          ev.preventDefault();
          handleAction('evaluate');
          updateView();
          return;
        }
        if (k === 'Backspace') {
          ev.preventDefault();
          handleAction('back');
          updateView();
          return;
        }
        if (k.toLowerCase() === 'c') {
          // 'c' to clear
          ev.preventDefault();
          handleAction('clear');
          updateView();
          return;
        }
      });

      // initialize
      updateView();
    })();
  </script>
</body>
</html>

}
```


## Related

Here are some related projects

[Awesome README](https://github.com/matiassingers/awesome-readme)


## Lessons Learned

💡 Learning Outcomes

By building this calculator, you’ll learn how to:

Use JavaScript to manipulate the DOM in real time

Handle user interactions using event listeners

Implement arithmetic operations programmatically

Manage state and update the display dynamically

Design responsive layouts using CSS Grid or Flexbox

🚀 Project Improvements (Optional)

You can enhance this project by adding:

Scientific mode (sin, cos, tan, square root, power, etc.)

Calculation history

Dark/Light mode toggle

Memory buttons (M+, M−, MR)

Theme customization

