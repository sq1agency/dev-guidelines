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
We formed our branching structure around the way Pivotal Tracker handles our
project progress tracking. In Pivotal Tracker, you encounter the following terms:

|Term|What Is It?|
|----|-----------|
|Bug|A bug is really what you'd expect it to be: a bug. Something just isn't right with the code, and something must be done about it!|
|Feature|A new addition to the code, be it functional or visual. We try to keep these features as small and as modular as possible. Single responsibility principle should be taken to feature development.|
|Chore|Sometimes we just have to do little tasks that make an impact on our code but aren't really feature additions. Maybe we need to update the README or change the way the code initializes.|
|Epic|A collection of __Features__, __Bugs__, and __Chores__ (often summarized as __stories__). These should be tied to larger code pushes, such as new pages, forms, API endpoints. We try to keep these fairly small as well.|

### Environments and Main Branches
We utilize three different code environments, and these are considered our __main__
branches. __The master, staging, and development branches should not be deleted,
and pull requests should always be used when merging into them.__

|Main Branch|What Is It Used For?|
|-----------|--------------------|
|master|Our production branch. This should only contain code that has been QA'd and has been verified as completely stable.|
|staging|Our staging branch. This should contain code that is stable, but this should be the environment utilized for QA and final client approval before moving to production.|
|development|Our development branch. This environment is expected to be less stable, where large sets of features, epics, and bugs are tried out in tandem on the server configuration.|

## Epic Development Branching
As an __Epic__ is expected to be a set of Features, Bugs, and Chores, you'll
always branch off the main __development__ branch when developing an Epic.

The following naming convention is utilized when creating __Epic__ branches:

`epic/PIVOTAL-EPIC-NUMBER/brief-description`

Where:

- __PIVOTAL-EPIC-NUMBER__ is the Pivotal Tracker ID for the Epic being developed.
- __brief-description__ is a very short description of the Epic being developed. Keep this very short and replace any spaces with a dash. Remember other people may have to type it a lot!

Epics can be merged back into the main __development__ branch utilizing a pull-request.

## Feature Development Branching
Ideally, and in most cases, __Features__ will belong to an Epic. If a Feature
belongs to an Epic, branch the Feature off of that Epic's branch. If a Feature
does not belong to an Epic, branch off the main __development__ branch.

The following naming convention is utilized when creating __Epic__ branches:

`feature/PIVOTAL-FEATURE-NUMBER/brief-description`

Where:

- __PIVOTAL-FEATURE-NUMBER__ is the Pivotal Tracker ID for the Feature being developed.
- __brief-description__ is a very short description of the Feature being developed. Keep this very short and replace any spaces with a dash. Remember other people may have to type it a lot!

Feature branches should be merged back into the branches they were branched from utilizing a pull-request.

## Bug Development Branching
As __Bugs__ can and do appear at every step in a project's life-cycle, we handle
them with a bit more flexibility. Whenever possible, try to resolve Bugs off of
the main __development__ branch, but when that is impossible (if there are Features
or Epics on development not ready to migrate to staging), branch off of the main
__staging__ branch. If branching off of __staging__ is also impossible, branch off of __master__.

A good rule to remember: Start the farthest you can away from __master__ and
move closer as needed. If you don't know what to branch a Bug off of, ask your PM
or tech lead!

The following naming convention is utilized when creating __Bug__ branches off
the main __development__, Feature, or Epic branch:

`bug/PIVOTAL-BUG-NUMBER/brief-description`

The following naming convention is utilized when creating __Bug__ branchess off
the main __master__ or __staging__ branches:

`hotfix/PIVOTAL-BUG-NUMBER/brief-description`

Where:

- __PIVOTAL-BUG-NUMBER__ is the Pivotal Tracker ID for the Bug being patched.
- __brief-description__ is a very short description of the Bug being patched. Keep this very short and replace any spaces with a dash. Remember other people may have to type it a lot!

Feature branches should be merged into the branches they were branched from utilizing a pull-request.
