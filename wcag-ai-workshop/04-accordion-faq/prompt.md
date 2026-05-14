# Exercise 4: Accordion FAQ

You are an accessibility-focused front-end engineer.

Convert the following FAQ accordion into WCAG 2.2 AA compliant HTML, CSS, and JavaScript.

Focus on:
- Each accordion question should be a real button
- Each button should be inside a heading
- Use aria-expanded
- Use aria-controls
- Each answer region should have a clear relationship to its button
- All accordion controls must work with keyboard
- Visible focus styles
- Sufficient color contrast
- Do not rely on mouse-only interaction

Rules:
- Prefer semantic HTML and native button behavior.
- Use ARIA only to expose expanded and collapsed state.
- Return one complete HTML file.
- Return only the corrected HTML, no explanation.

Here is the broken HTML:

```html
<!DOCTYPE html>
<html>
<head>
  <title>FAQ</title>
  <style>
    .question { font-weight: bold; cursor: pointer; background: #eee; padding: 10px; margin-top: 8px; }
    .answer { display: none; padding: 10px; }
  </style>
  <script>
    function toggleAnswer(id) {
      var answer = document.getElementById(id);
      answer.style.display = answer.style.display === "block" ? "none" : "block";
    }
  </script>
</head>
<body>
  <h1>Frequently Asked Questions</h1>
  <div class="question" onclick="toggleAnswer('a1')">What is your return policy?</div>
  <div id="a1" class="answer">You can return items within 30 days.</div>
  <div class="question" onclick="toggleAnswer('a2')">Do you ship internationally?</div>
  <div id="a2" class="answer">Yes, we ship to selected countries.</div>
  <div class="question" onclick="toggleAnswer('a3')">How do I contact support?</div>
  <div id="a3" class="answer">Email support@example.com.</div>
</body>
</html>
```
