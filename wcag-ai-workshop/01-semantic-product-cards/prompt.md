# Exercise 1: Semantic product cards

You are an accessibility-focused front-end engineer.

Convert the following product card HTML into WCAG 2.2 AA compliant HTML.

Focus on:
- Semantic page structure
- Proper heading hierarchy
- Accessible product card structure
- Meaningful image alt text
- Real buttons instead of clickable divs
- Visible keyboard focus
- Sufficient color contrast
- Clear button names such as “Buy Desk Lamp” instead of only “Buy”

Rules:
- Prefer semantic HTML over ARIA.
- Use ARIA only if native HTML is not enough.
- Return one complete HTML file.
- Return only the corrected HTML, no explanation.

Here is the broken HTML:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Product Cards</title>
  <style>
    .card {
      display: inline-block;
      width: 220px;
      border: 1px solid #ccc;
      padding: 12px;
      margin: 10px;
    }

    .title {
      font-size: 18px;
      font-weight: bold;
    }

    .button {
      background: #ddd;
      color: #999;
      padding: 8px;
      cursor: pointer;
      text-align: center;
    }
  </style>
</head>
<body>
  <div class="title">Featured Products</div>

  <div class="card">
    <img src="lamp.jpg" width="200">
    <div class="title">Desk Lamp</div>
    <div>Bright LED lamp for your desk.</div>
    <div class="button">Buy</div>
  </div>

  <div class="card">
    <img src="chair.jpg" width="200">
    <div class="title">Office Chair</div>
    <div>Comfortable chair for long workdays.</div>
    <div class="button">Buy</div>
  </div>
</body>
</html>
```
