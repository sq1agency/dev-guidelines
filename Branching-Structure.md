---
layout: page
title: Branching Structure
---

At Sq1 we try to make order in the chaos. Despite the fact that our projects can
vary widely by size and type, we try to keep processes the same. This is how we
handle our branching structure in Git.

_New to Git? Try out this [awesome tutorial](https://try.github.io/levels/1/challenges/1)!_

![Branching Structure Overview]({{ site.baseurl }}public/img/branching-structure-overview.png)

## Basic Concept and Terms
We formed our branching structure around the way [Pivotal Tracker](https://www.pivotaltracker.com/dashboard) handles our
project progress tracking. In Pivotal Tracker, you encounter the following terms:

|Term|What Is It?|
|----|-----------|
|Bug|A bug is really what you'd expect it to be: a bug. Something just isn't right with the code, and something must be done about it!|
|Feature|A new addition to the code, be it functional or visual. We try to keep these features as small and as modular as possible. Single responsibility principle should be observed with feature development.|
|Chore|Sometimes we have to do little tasks that make an impact on our code but aren't really feature additions. Maybe we need to update the `README` or change the way the code initializes.|
|Epic|A collection of __Features__, __Bugs__, and __Chores__ (often summarized as __stories__). These should be tied to larger code pushes, such as new pages, forms, and API endpoints. We try to keep these fairly small as well.|

### Environments and Main Branches
We utilize three different code environments, and these are considered our _main
branches_.

__Important: The master, staging, and development branches should not be deleted,
and pull requests should always be used when merging into them.__

|Main Branch|What Is It Used For?|
|-----------|--------------------|
|master|Our production branch. This should only contain code that has been QA'd and verified as completely stable.|
|staging|Our staging branch. This should contain code that is stable as well. This branch should be the environment utilized for QA and final client approval before moving to production.|
|development|Our development branch. This environment is expected to be less stable.  You can expect there to be large sets of features, epics, and bugs that are being tried out in tandem on the server configuration.|

## Epic Development Branching
As an __Epic__ is expected to be a set of __Features__, __Bugs__, and __Chores__, you'll
always branch off the main _development_ branch when developing an __Epic__.

The following naming convention is utilized when creating an __Epic__ branch:

`epic/PIVOTAL-EPIC-NUMBER/brief-description`

Where:

- __PIVOTAL-EPIC-NUMBER__ is the Pivotal Tracker ID for the __Epic__ being developed.
- __brief-description__ is a very short description of the __Epic__ being developed. Keep this very short and replace any spaces with a dash. Remember other people may have to type it a lot!

Epics can be merged back into the main _development_ branch utilizing a pull-request.

## Feature Development Branching
Ideally, and in most cases, __Features__ will belong to an __Epic__. If a __Feature__
belongs to an __Epic__, branch the __Feature__ off of that __Epic__'s branch. If a __Feature__
does not belong to an __Epic__, branch off the main _development_ branch.

The following naming convention is utilized when creating __Epic__ branches:

`feature/PIVOTAL-FEATURE-NUMBER/brief-description`

Where:

- __PIVOTAL-FEATURE-NUMBER__ is the Pivotal Tracker ID for the __Feature__ being developed.
- __brief-description__ is a very short description of the __Feature__ being developed. Keep this very short and replace any spaces with a dash. Remember other people may have to type it a lot!

__Feature__ branches should be merged using a pull request.  Always remember to merge back into the branch you branched from.

## Bug Development Branching
As __Bugs__ can and do appear at every step in a project's life-cycle, we handle
them with a bit more flexibility. Whenever possible, try to resolve __Bugs__ off of
the main _development_ branch, but when that is impossible (if there are __Features__
or __Epics__ on development not ready to migrate to staging), branch off of the main
_staging_ branch. If branching off of _staging_ is also impossible, branch off of _master_.

A good rule to remember: Start the farthest you can away from _master_ and
move closer as needed. If you don't know what to branch a __Bug__ off of, ask your PM
or tech lead!

The following naming convention is utilized when creating __Bug__ branches off
the main _development_, __Feature__, or __Epic__ branch:

`bug/PIVOTAL-BUG-NUMBER/brief-description`

The following naming convention is utilized when creating __Bug__ branches off
the main _master_ or _staging_ branches:

`hotfix/PIVOTAL-BUG-NUMBER/brief-description`

Where:

- __PIVOTAL-BUG-NUMBER__ is the Pivotal Tracker ID for the __Bug__ being patched.
- __brief-description__ is a very short description of the __Bug__ being patched. Keep this very short and replace any spaces with a dash. Remember other people may have to type it a lot!

__Feature__ branches should be merged using a pull request.  Always remember to merge back into the branch you branched from.
