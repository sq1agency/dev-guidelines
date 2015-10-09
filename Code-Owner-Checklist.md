---
layout: page
title: The Code Owner's Checklist
---

In this document is a nifty set of checklists that every Code Owner should utilize when building and maintaining a repo.

## Setting Up A Repository
- Is there a reason not to use a [starter-kit]()? If there isn't, then use one!
- Create a `README.md` file.
- Create a `CONTRIBUTING.md` file.
- Create the `needs review` tag.
- Make sure you have an `.eslintrc` and `.editorconfig` file!
- Ask a few other devs to try and set up your application using just the instructions in your `README.md`
- Tweak your `README.md` as needed. Repeat previous checklist until satisfied devs are had.

## README.md Checklist
Order is kind of important with this one, so these are listed from top to bottom. (You can also check out this [Template README.md](Template README.md).)

- Project name
- Brief overview of repository
- Code Owner(s)
- Link to relevant project management system (Pivotal Tracker, Sprint.ly, Waffle.io, etc.)
- Links to relevant wiki documentation (APIs, Gotchas, etc.)
- Installation instructions
- Development Usage
- Deployment Process
- Technologies Used

## Code Review Checklist
Code review can be tedious, but it's incredibly important to the health and maintainability of code, and it also helps out your peers! Ask yourself these questions as you review code and if any of the questions are a "No", don't accept the pull request, politely and thoroughly mention the issues with the code, and assign the pull request back to the originating user.

- Does the pull request description include a thorough description of changes included within the pull request?
- Does the code meet the repo's style guide requirements? (Does it pass linting?)
- Is the code well commented/documented?
- Does the code make sense?
- Does the code pass all required unit tests?
