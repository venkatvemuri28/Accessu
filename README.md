# WCAG + LLM Workshop Exercises
## Goal
Use AI tools to improve broken HTML and make it more accessible.
You will copy each exercise into an LLM, ask it to fix the accessibility issues, then manually test the result on your desktop.
## Tools to use
Use any of these AI tools:
- Google: `google.com`
- ChatGPT: `chat.com`
- Microsoft Copilot: `https://copilot.microsoft.com/`
## How to do each exercise
Each exercise folder has:
```text
index.html
prompt.md

Steps:

1. Open index.html.
2. Review the broken HTML.
3. Open prompt.md.
4. Copy the prompt.
5. Paste the prompt into ChatGPT, Copilot, or another LLM.
6. Paste the full index.html code under the prompt.
7. Ask the LLM to return corrected HTML.
8. Replace the old index.html with the new version.
9. Open the page in a desktop browser.
10. Manually test the result.

Manual desktop testing checklist

After the LLM creates the new HTML, test it yourself.

Check:

* Can you use the page with only the keyboard?
* Can you move forward with Tab?
* Can you move backward with Shift + Tab?
* Can you activate buttons with Enter or Space?
* Is the focus indicator visible?
* Are buttons and links clear?
* Do images have useful alt text?
* Do form fields have labels?
* Do modals, tabs, dropdowns, and menus work with keyboard?
* Can modals be closed with Escape?
* Does focus return to the correct place after closing a modal?
* Are errors connected to the right fields?
* Are dynamic updates announced when using VoiceOver?

VoiceOver testing on Mac

Turn VoiceOver on or off:

Command + F5

VoiceOver uses this modifier:

Control + Option

This is often written as VO.

Useful commands:

VO + Right Arrow    Read next item
VO + Left Arrow     Read previous item
VO + U              Open rotor
Tab                 Move to next interactive control
Shift + Tab         Move to previous interactive control
Enter or Space      Activate a control
Escape              Close menus or modals

Exercise order

1. Product cards
2. Dropdown navigation
3. Tabs
4. Accordion FAQ
5. Modal dialog
6. Data table
7. Toast notification
8. Checkout wizard
9. Filterable product grid
10. Final dashboard app

Important note

AI can help generate accessible code, but it can still make mistakes.

Use this workflow:

Prompt → Generate → Review → Manually Test → Fix

The goal is not to trust the AI. The goal is to learn how to use AI as a helper while you verify the experience yourself.
