# Exercise 3: Accessible tabs component

You are an accessibility-focused front-end engineer.

Convert the following product details tabs into a WCAG 2.2 AA compliant tabs component.

Focus on:
- Correct tab semantics
- role="tablist"
- role="tab"
- role="tabpanel"
- aria-selected
- aria-controls
- Correct relationship between each tab and its panel
- Keyboard support with ArrowLeft, ArrowRight, Home, and End
- Enter or Space activates a tab
- Only the active tab panel is visible
- Visible focus styles
- Sufficient color contrast

Rules:
- Use ARIA because tabs are a custom interactive component.
- Keep the implementation simple and readable for workshop students.
- Return one complete HTML file.
- Return only the corrected HTML, no explanation.

Here is the broken HTML:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Product Details Tabs</title>
  <style>
    .tab { display: inline-block; padding: 10px; background: #eee; cursor: pointer; }
    .panel { display: none; padding: 15px; border: 1px solid #ccc; }
    #details { display: block; }
  </style>
  <script>
    function showPanel(id) {
      document.getElementById("details").style.display = "none";
      document.getElementById("shipping").style.display = "none";
      document.getElementById("reviews").style.display = "none";
      document.getElementById(id).style.display = "block";
    }
  </script>
</head>
<body>
  <h1>Wireless Keyboard</h1>
  <div>
    <span class="tab" onclick="showPanel('details')">Details</span>
    <span class="tab" onclick="showPanel('shipping')">Shipping</span>
    <span class="tab" onclick="showPanel('reviews')">Reviews</span>
  </div>
  <div id="details" class="panel"><p>Compact wireless keyboard with long battery life.</p></div>
  <div id="shipping" class="panel"><p>Ships in 3 to 5 business days.</p></div>
  <div id="reviews" class="panel"><p>Rated 4.5 out of 5 by customers.</p></div>
</body>
</html>
```
