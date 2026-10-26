---
doc: spec
status: approved
---

# Inbox Sorter — Technical Spec

## How This Works, In Plain Language
The whole app is one file, `index.html`. It holds the page layout (HTML), the colors and fonts (CSS), and the logic (JavaScript). When the user clicks "Sort my inbox," the code reads the pasted list, applies the suggestion rule, and shows three columns. The choices are saved in the browser's storage so they survive a refresh.

We chose one file because it's the simplest thing that works, needs no install, and is easy to explain.

## The Core Journey Through the System
1. The user opens `index.html` in a browser.
2. The user pastes senders, one per line as `sender, how often`, and clicks "Sort my inbox." If the box is empty, the app shows "Please paste at least one sender."
3. The code suggests a decision for each sender and shows the review screen with three columns.
4. The user clicks Keep or Filter on any sender. The choice is saved in the browser.
5. After a refresh, the saved choices are still there.
PRD ref: `prd.md > The Core Journey`

## Stack
- HTML, CSS, and JavaScript, with no libraries.
- Browser storage: `localStorage`. Docs: https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage
- Reason: nothing to install, and it runs anywhere. Tradeoff: no sync between devices.

## Where It Runs and How Someone Tries It
- Runs in any modern browser (Chrome, Edge, Firefox).
- To try it: double-click `index.html`.
- For the demo video: record the page sorting a sample list of 5 senders.

## Look and Feel
- White background, dark gray text, easy on the eyes.
- Headings in Georgia. Body text and buttons in Arial.
- Blue main button, green Keep, yellow Newsletters, red Spam.

## Components
### Paste screen
Title, the sender box, and the "Sort my inbox" button.
PRD ref: `prd.md > Screens and Layout`

### Suggestion logic
- "daily" → Spam column, suggested Filter.
- "weekly" → Newsletters column, suggested Filter.
- Any other value, or no value → Keep column, suggested Keep.
- Keep = the user marks the sender as important. Filter = the sender is removed.
PRD ref: `prd.md > Features and Behavior`

### Review screen
Three columns with Keep and Filter buttons for each sender.
PRD ref: `prd.md > Screens and Layout`

## Data Model
One object per sender: `{ sender, howOften, decision }`. The list is saved in `localStorage` under one key. When the user returns, the list loads from there.

## File Structure
