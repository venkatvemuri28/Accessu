# Exercise 8: Multi-step checkout wizard

You are an accessibility-focused front-end engineer.

Convert the following multi-step checkout wizard into WCAG 2.2 AA compliant HTML, CSS, and JavaScript.

Focus on:
- Clear page and step headings
- Accessible progress indication
- Do not communicate progress by color alone
- Proper labels for every form field
- Use fieldset and legend where helpful
- Validate required fields before moving to the next step
- Display accessible error messages
- Use aria-describedby for field help and errors
- Move focus to the new step heading after step changes
- Announce step changes to screen reader users
- Real buttons for Next, Back, and Submit
- Visible focus styles
- Sufficient color contrast

Rules:
- Keep the wizard simple enough for workshop students.
- Prefer semantic HTML over ARIA.
- Use ARIA for announcements and error relationships where needed.
- Return one complete HTML file.
- Return only the corrected HTML, no explanation.

Here is the broken HTML:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Checkout Wizard</title>
  <style>
    .step { display: none; }
    #step1 { display: block; }
    .progress span { color: #999; margin-right: 10px; }
    .active { color: green; }
  </style>
  <script>
    function nextStep(current, next) {
      document.getElementById(current).style.display = "none";
      document.getElementById(next).style.display = "block";
    }
  </script>
</head>
<body>
  <h1>Checkout</h1>
  <div class="progress"><span class="active">1 Shipping</span><span>2 Payment</span><span>3 Review</span></div>
  <div id="step1" class="step"><h2>Shipping</h2><input placeholder="Full name"><input placeholder="Address"><button onclick="nextStep('step1', 'step2')">Next</button></div>
  <div id="step2" class="step"><h2>Payment</h2><input placeholder="Card number"><input placeholder="Expiration date"><button onclick="nextStep('step2', 'step3')">Next</button></div>
  <div id="step3" class="step"><h2>Review</h2><p>Review your order before submitting.</p><button>Submit Order</button></div>
</body>
</html>
```
