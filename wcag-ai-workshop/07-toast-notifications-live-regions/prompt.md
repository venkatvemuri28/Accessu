# Exercise 7: Toast notifications and live regions

You are an accessibility-focused front-end engineer.

Convert the following toast notification example into WCAG 2.2 AA compliant HTML, CSS, and JavaScript.

Focus on:
- Properly associated form labels
- A real button for saving
- A live region for the save confirmation
- Use role="status" or aria-live="polite"
- Ensure the message is announced to screen reader users
- Do not remove the message too quickly
- Do not require users to chase focus to the toast
- Provide visible focus styles
- Ensure sufficient color contrast

Rules:
- The toast should be helpful but not disruptive.
- Prefer polite announcements for successful save messages.
- Return one complete HTML file.
- Return only the corrected HTML, no explanation.

Here is the broken HTML:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Toast Notification</title>
  <style>
    #toast { display: none; position: fixed; bottom: 20px; right: 20px; background: #333; color: white; padding: 12px; }
  </style>
  <script>
    function saveProfile() {
      document.getElementById("toast").innerText = "Profile saved";
      document.getElementById("toast").style.display = "block";
      setTimeout(function () { document.getElementById("toast").style.display = "none"; }, 3000);
    }
  </script>
</head>
<body>
  <h1>Edit Profile</h1>
  <label>Name</label>
  <input type="text" value="Sam Rivera">
  <button onclick="saveProfile()">Save</button>
  <div id="toast"></div>
</body>
</html>
```
