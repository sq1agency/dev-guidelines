---
layout: page
title: Pull Requests and Code Reviews
---

Code Reviews are the key for quality control in project code and individual
developer growth. We utilize Github's [pull requests](https://help.github.com/articles/using-pull-requests/)
to handle Code Reviews and branch merging. However, anyone can request a code review
for a specific commit at any time.

## Making a Great Pull Request
Since we utilize Pull Requests to both handle merging and code reviews, it's imperative
that you work to craft an informative and useful pull request. When creating a pull
request, try to remember to include the following:

- Short, descriptive title
- Brief overview of what you're trying to accomplish
- List of fixes and features broken out as concisely as possible
- Caveats the reviewer should keep in mind when reviewing

In general, assume the person reviewing the code has no insight into the project.

Once you've crafted and opened your pull request, assign someone from the team
(anyone can review anyone else's code) with a skill set that can properly look
over the changed code.

__Remember to ping your reviewer on Slack__ to make sure they're available! Please
give the reviewer an hour or so to review. We're all rather busy.

Please note that sometimes pull requests are only as good as the commits made within
them. __Remember to keep your commits nice and small to make review much easier.__

## Reviewing Code
As any member of the team can (and will be expected to) review code for other team
members, everyone needs to know some best practices for reviewing code.

You do NOT need a full understanding of a project to review code. All code
reviews should be easily digestible by someone who is not the contributor.

Here are some things that a code review is __not__:

- __Personal__: Try to refer to the person making the PR as "the contributor" to create a sense of personal detachment
- __A Place for Style/Design Decisions__: You may not agree with the way a
contributor has styled or architected their code, but if no agreement was not
made (and documented) beforehand, this is not the place to add rules and design
constructs to a project.
- __Painful__: Think "constructive criticism" when doing a code review. Try to
highlight well executed things and always, always offer suggestions and tips for
resolution for problems you see in the code.
- __Project QA__: Remember that the reviewer is not the QA Engineer. Reviewers should
only be taking the specific code being changed into consideration when reviewing
the code, and shouldn't need to pull down the code locally to run or test the
environment. Contributors, do your own local QA!

Here are some things that a code review __should be__:

- __Constructive__: Code reviews are a great place to nurture mentor relationships.
Give ideas for improvement, teach concept.
- __Concise__: Try not to launch into rants, and keep it to what the reviewer and/or
the contributor need to know.
- __A Place for Quality Control__: Check both the project's and team's styleguides
and any appropriate tools (.editorconfig, .eslintrc, etc.) to ensure the code adheres
to the given guidelines.

## Waiting for a Code Review
Although turn around time will usually be pretty quick, with team members sometimes
in and out of meetings, some pull requests may take longer to resolve than others.
If needed, you can always assign a pull request to another team member who is available
to review your code. In general, unless there is a hotfix or major issue that needs to
be resolved, a little bit of wait time isn't a bad thing.
