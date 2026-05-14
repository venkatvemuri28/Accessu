# Exercise 5: Modal dialog with focus management

You are an accessibility-focused front-end engineer.

Convert the following modal dialog example into WCAG 2.2 AA compliant HTML, CSS, and JavaScript.

Focus on:
- Use a real button to open the modal
- Use real buttons inside the modal
- Add role="dialog"
- Add aria-modal="true"
- Add aria-labelledby for the modal title
- Move focus into the modal when it opens
- Trap keyboard focus inside the modal while open
- Close the modal with the Escape key
- Return focus to the original trigger button when the modal closes
- Prevent keyboard users from tabbing into the page behind the modal
- Provide visible focus styles
- Ensure sufficient color contrast

Rules:
- Use ARIA because this is a custom modal dialog.
- Keep the JavaScript simple and understandable.
- Return one complete HTML file.
- Return only the corrected HTML, no explanation.

Here is the broken HTML:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Modal Example</title>
  <style>
    .modal { display: none; position: absolute; top: 80px; left: 80px; background: white; border: 1px solid black; padding: 20px; width: 300px; }
    .overlay { display: none; position: fixed; inset: 0; background: rgba(0,0,0,0.3); }
    .button { background: #ccc; padding: 10px; cursor: pointer; display: inline-block; }
  </style>
  <script>
    function openModal() { document.getElementById("overlay").style.display = "block"; document.getElementById("modal").style.display = "block"; }
    function closeModal() { document.getElementById("overlay").style.display = "none"; document.getElementById("modal").style.display = "none"; }
  </script>
</head>
<body>
  <h1>Account Settings</h1>
  <div class="button" onclick="openModal()">Delete Account</div>
  <div id="overlay" class="overlay"></div>
  <div id="modal" class="modal">
    <div>Confirm Delete</div>
    <p>Are you sure you want to delete your account?</p>
    <div class="button" onclick="closeModal()">Cancel</div>
    <div class="button">Delete</div>
  </div>
</body>
</html>
```
