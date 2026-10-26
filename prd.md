---
doc: prd
status: approved
---

# Inbox Sorter — Product Requirements

A browser page where the user marks the emails that matter, and everything else gets filtered out.
Source: `scope.md > The Core Loop, The POC Boundary`

## The Core Journey
1. The user opens the page and sees a box to paste a sender list.
2. The user pastes one sender per line and clicks "Sort my inbox."
3. The user marks the senders that matter.
4. The app suggests a decision for each unmarked sender.
5. The user reviews the suggestions, changes any they disagree with, and sees the filtered list.
Success: the user ends with a list of senders to keep and a list to filter, in under 5 minutes.

## Screens and Layout
- **Paste screen:** title "Inbox Sorter," a large box for the sender list, and a blue "Sort my inbox" button.
- **Review screen:** three columns (green Keep, yellow Newsletters, red Spam). Each sender shows a short reason and two buttons: "Keep" and "Filter."

## Look and Feel
- White background, easy on the eyes, simple, with a few colors like Google Slides.
- Headings: Georgia, dark gray. Main text and buttons: Arial.
- Colors: blue for the main button, green for Keep, yellow for Newsletters, red for Spam.

## Features and Behavior

### Marking and suggesting
- The user marks senders as important.
- Unmarked senders get a suggestion:
  - A person who doesn't email on a schedule: kept.
  - A sender that emails weekly or more often: filtered.
- The user can change any suggestion with the "Keep" or "Filter" buttons.

## States and Boundaries
- **First use:** the paste screen is empty.
- **No marks:** clicking "Sort my inbox" with nothing marked shows "Please mark at least one sender" and doesn't sort.
- **Saved choices:** the user's decisions are saved in their browser and still there after a refresh. Nothing leaves the device.

## Product Decisions
- The user decides what matters; the app only suggests. Reason: the user stays in control.
- Nothing is sent to a server. Reason: privacy, and no login is needed.
- Clicking sort with nothing marked does nothing except show a message. Reason: the user stays in control, and the app doesn't guess.

## What We're Building
- Paste a sender list, mark senders, see suggestions, change them, and see the filtered result.
- Save choices in the browser.

## Deferred From the POC
- Gmail or Outlook login: needs accounts and permissions.
- Saving choices across devices: needs an account or server.

## Possible Later Enhancements
- Read emails directly from Gmail or Outlook.
- Unsubscribe links for newsletters.

## Non-Goals
- Sending, deleting, or unsubscribing from emails: risky and out of scope for a first version.
- Logging in or storing data on a server.

## Open Questions
- None that block the technical plan.