# Exercise 9: Filterable product grid

You are an accessibility-focused front-end engineer.

Convert the following filterable product grid into WCAG 2.2 AA compliant HTML, CSS, and JavaScript.

Focus on:
- Proper label for the search input
- Helpful instructions for filtering
- Semantic product list or product card structure
- Meaningful image alt text
- Accessible result count
- Announce result count changes with aria-live
- Preserve keyboard accessibility
- Ensure focus is not unexpectedly moved while typing
- Use sufficient color contrast
- Use proper headings for product names

Rules:
- Prefer semantic HTML.
- Use ARIA only for live result updates if needed.
- Return one complete HTML file.
- Return only the corrected HTML, no explanation.

Here is the broken HTML:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Product Filter</title>
  <style>
    .product { border: 1px solid #ccc; margin: 10px; padding: 10px; }
  </style>
  <script>
    function filterProducts() {
      var query = document.getElementById("search").value.toLowerCase();
      var products = document.querySelectorAll(".product");
      products.forEach(function(product) {
        if (product.innerText.toLowerCase().includes(query)) product.style.display = "block";
        else product.style.display = "none";
      });
    }
  </script>
</head>
<body>
  <h1>Products</h1>
  <input id="search" placeholder="Search products" onkeyup="filterProducts()">
  <div class="product"><img src="keyboard.jpg" width="120"><div>Keyboard</div><div>$45</div></div>
  <div class="product"><img src="mouse.jpg" width="120"><div>Mouse</div><div>$25</div></div>
  <div class="product"><img src="monitor.jpg" width="120"><div>Monitor</div><div>$199</div></div>
</body>
</html>
```
