---
doc: scope
status: approved
---

# Inbox Sorter

A browser page where you mark the emails that matter, and everything else gets filtered out.

## The Unique Kernel
The user decides what matters. The app only suggests, and the user always has the final say.

## Who It's For
Someone with hundreds of unread emails, mostly newsletters and promotions, who wants to clear them quickly without reading each one.

## The Core Loop
The user pastes a list of senders, marks the ones that matter, reviews the suggestions for the rest, and sees the filtered list.

## Inspiration & Identity
A clean, simple screen that asks which emails are important, then removes the rest.

## Why This Matters to the Learner
Cluttered inboxes are a common everyday problem, and it's a project the learner can explain clearly.

## What "Working" Looks Like
A user pastes a list of senders, marks the important ones, sees the suggestions for the others, changes any of them, and sees the filtered result. It runs on one page in the browser.

## The POC Boundary
- Paste a list of senders
- Mark senders as important
- Suggest a decision for unmarked senders: a person who doesn't email on a schedule is kept; a sender that emails weekly or more often is filtered
- Let the user change any decision
- Save choices in the user's own browser

## Later
- Reading emails directly from Gmail or Outlook
- Sharing or saving between devices

## Explicitly Cut
- Login and accounts: they need a server and would take most of the time
- Sending, deleting, or unsubscribing from emails: risky and needs permissions
- A database or server: the app runs in the browser only