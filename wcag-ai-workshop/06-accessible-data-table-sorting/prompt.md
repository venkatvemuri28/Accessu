# Exercise 6: Accessible data table with sorting controls

You are an accessibility-focused front-end engineer.

Convert the following orders table into WCAG 2.2 AA compliant HTML, CSS, and JavaScript.

Focus on:
- Add a table caption
- Use thead and tbody
- Use th with scope="col"
- Put real buttons inside sortable column headers
- Communicate sort state accessibly
- Use aria-sort where appropriate
- Announce sorting changes to screen reader users
- Do not communicate status by color alone
- Improve color contrast
- Preserve readable visual design
- Make all sorting controls keyboard accessible

Rules:
- Prefer semantic table markup.
- Use ARIA only where it helps communicate dynamic sorting state.
- Return one complete HTML file.
- Return only the corrected HTML, no explanation.

Here is the broken HTML:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Orders Table</title>
  <style>
    th { cursor: pointer; background: #eee; }
  </style>
  <script>
    function sortTable(column) { alert("Sorted by " + column); }
  </script>
</head>
<body>
  <h1>Orders</h1>
  <table>
    <tr><td>Order ID</td><td>Customer</td><td>Status</td><td>Total</td></tr>
    <tr><td>1001</td><td>Ana Patel</td><td style="color:green;">Paid</td><td>$42.00</td></tr>
    <tr><td>1002</td><td>Marcus Lee</td><td style="color:red;">Failed</td><td>$18.00</td></tr>
    <tr><td>1003</td><td>Jordan Kim</td><td style="color:orange;">Pending</td><td>$75.00</td></tr>
  </table>
  <p>Click column names to sort.</p>
</body>
</html>
```
