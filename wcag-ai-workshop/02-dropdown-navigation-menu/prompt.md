# Exercise 2: Dropdown navigation menu

You are an accessibility-focused front-end engineer.

Convert the following dropdown navigation menu into WCAG 2.2 AA compliant HTML, CSS, and JavaScript.

Focus on:
- Semantic navigation using nav
- A real button for opening the dropdown
- aria-expanded and aria-controls
- Keyboard support
- Escape key closes the dropdown
- Focus remains logical when opening and closing the menu
- Visible focus styles
- Sufficient color contrast
- Descriptive link text

Rules:
- Prefer native HTML behavior where possible.
- Use ARIA only where it improves the custom dropdown behavior.
- Do not create a hover-only menu.
- Return one complete HTML file.
- Return only the corrected HTML, no explanation.

Here is the broken HTML:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Dropdown Menu</title>
  <style>
    .menu { background: #333; padding: 10px; }
    .menu a, .dropdown-button { color: white; margin-right: 20px; cursor: pointer; }
    .submenu { display: none; position: absolute; background: white; border: 1px solid #ccc; padding: 10px; }
    .submenu a { color: black; display: block; margin: 8px; }
  </style>
  <script>
    function toggleMenu() {
      var menu = document.getElementById("products-menu");
      menu.style.display = menu.style.display === "block" ? "none" : "block";
    }
  </script>
</head>
<body>
  <div class="menu">
    <a href="#">Home</a>
    <span class="dropdown-button" onclick="toggleMenu()">Products</span>
    <a href="#">Support</a>
  </div>
  <div id="products-menu" class="submenu">
    <a href="#">Laptops</a>
    <a href="#">Monitors</a>
    <a href="#">Accessories</a>
  </div>
  <h1>Welcome</h1>
</body>
</html>
```
