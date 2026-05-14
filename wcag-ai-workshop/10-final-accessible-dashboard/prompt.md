# Exercise 10: Final accessible dashboard app

You are an accessibility-focused front-end engineer.

Convert the following admin dashboard into a WCAG 2.2 AA compliant web app.

This is the final workshop exercise, so apply all accessibility improvements from the earlier exercises.

Focus on:
- Semantic layout with header, nav, main, sections, and footer if appropriate
- Skip link
- Proper heading hierarchy
- Accessible navigation
- Sufficient color contrast
- Visible focus styles
- Accessible summary cards
- Accessible tabs with correct ARIA semantics
- Keyboard support for tabs using ArrowLeft, ArrowRight, Home, and End
- Accessible data table with caption, thead, tbody, and column headers
- Do not communicate status by color alone
- Real buttons instead of clickable divs or spans
- Accessible modal dialog
- role="dialog"
- aria-modal="true"
- aria-labelledby
- Focus moves into modal when opened
- Focus is trapped inside modal while open
- Escape key closes modal
- Focus returns to trigger after modal closes
- Accessible form labels
- Accessible validation errors
- aria-describedby for field errors
- aria-invalid for invalid fields
- Live region for save confirmation
- Avoid unnecessary ARIA where native HTML works

Rules:
- Return one complete HTML file with HTML, CSS, and JavaScript included.
- Keep the implementation understandable for workshop students.
- Do not use external libraries.
- Do not include explanations.
- Return only the corrected HTML.

Here is the broken HTML:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Admin Dashboard</title>
  <style>
    body { color: #999; font-family: Arial, sans-serif; }
    .nav { background: #222; padding: 10px; }
    .nav a { color: #777; margin-right: 15px; }
    .card { border: 1px solid #ddd; padding: 12px; margin: 10px; display: inline-block; width: 200px; }
    .tab { display: inline-block; background: #eee; padding: 10px; cursor: pointer; }
    .panel { display: none; border: 1px solid #ccc; padding: 15px; }
    #panel1 { display: block; }
    .modal { display: none; position: absolute; top: 100px; left: 100px; background: white; border: 1px solid black; padding: 20px; }
    .btn { background: #ddd; color: #aaa; padding: 8px; cursor: pointer; display: inline-block; }
    .error { color: red; }
  </style>
  <script>
    function showPanel(id) { document.getElementById("panel1").style.display = "none"; document.getElementById("panel2").style.display = "none"; document.getElementById(id).style.display = "block"; }
    function openModal() { document.getElementById("modal").style.display = "block"; }
    function closeModal() { document.getElementById("modal").style.display = "none"; }
    function saveSettings() { document.getElementById("toast").innerText = "Settings saved"; document.getElementById("toast").style.display = "block"; }
  </script>
</head>
<body>
  <div class="nav"><a href="#">Dashboard</a><a href="#">Reports</a><a href="#">Settings</a></div>
  <div>
    <div>Admin Dashboard</div>
    <div class="card"><div>Users</div><div>1,204</div></div>
    <div class="card"><div>Revenue</div><div>$42,300</div></div>
    <div><span class="tab" onclick="showPanel('panel1')">Orders</span><span class="tab" onclick="showPanel('panel2')">Settings</span></div>
    <div id="panel1" class="panel">
      <div>Recent Orders</div>
      <table><tr><td>Order</td><td>Status</td><td>Total</td></tr><tr><td>1001</td><td style="color:green;">Paid</td><td>$40</td></tr><tr><td>1002</td><td style="color:red;">Failed</td><td>$22</td></tr></table>
      <div class="btn" onclick="openModal()">View Details</div>
    </div>
    <div id="panel2" class="panel"><div>Settings</div><input placeholder="Display name"><input placeholder="Email"><p class="error">Email is required</p><div class="btn" onclick="saveSettings()">Save Settings</div></div>
  </div>
  <div id="modal" class="modal"><div>Order Details</div><p>Order 1001 was paid successfully.</p><div class="btn" onclick="closeModal()">Close</div></div>
  <div id="toast" style="display:none;"></div>
</body>
</html>
```
