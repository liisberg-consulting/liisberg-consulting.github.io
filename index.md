---
layout: default
title: Developers Handbook
permalink:
---

In an async, remote team, the importance of proper communication and discipline around procedure cannot be stressed enough.

For this reason, every developer on our team is REQUIRED to carefully read and adhere to the following rules of engagement.

Failure to comply will, after proper warning, result in exclusion from the team.

That said, once you understand and appreciate these guidelines, you will learn to love the simplicity and freedom they provide. No need for daily standups, no need for chats or skype conversations where information is easily lost. What's left is the ability to focus on implementing great features and finding the best solutions for the most interesting problems.

## Cheatsheet: Your everyday checklist

*   **Check Pivotal** - review stories in the current sprint, and reply to any new comments if neccesary.
*   **Pick the top-most story in Pivotal**.
    If you can't, add a blocker to the story with your reasons and move to the next story.
*   **Branch out** for each feature
*   **Commit and push everything** - Never leave code behind. Create a pull request and label it according to the state of the code (ready for review, need help, etc.).
*   Before you leave, **check Pivotal again** to make sure it's always up to date including any decisions or implementation details discussed in the chat.

## Philosophy

*   We work anytime from anywhere
*   We don't have meetings
*   We don't have deadlines

To enable this, we communicate using three different channels:

*   chatroom where conversations is logged
*   scrumboard where work items (stories) is defined and the development track is laid out
*   pull requests (see "Branches and pull requests" below) where specific solutions is being discussed and worked on

This way,

*   no-one needs to be online at a specific time
*   you can ignore pings and turn to the pinger later, staying in "the zone" if you happen to be there

# The Scrum Board

The scrum board is the center of the development process. Every feature, chore and bug lives here as stories. This means that **If it's not on the scrum board, it does not exist.**

We use pivotal tracker for scrum board ([http://www.pivotaltracker.com](http://www.pivotaltracker.com)). As a developer, you will be invited to participate actively with defining stories, prioritizing them and delivering them when they are done. The quality and effectiveness of your work will improve if you understand how you can participate to increase throughput and assure the correctness of stories.

It is therefore crucial that you understand the tool (Pivotal) and how we use it.

Here's a quick 8-minute intro to pivotal and the way we use it:
<video src="https://d2ddoduugvun08.cloudfront.net/items/0q0l3r0t433f3w230g0v/Screen%20Recording%202019-04-02%20at%2002.33%20PM.mov" controls style="display: block;height: auto;width: 100%;">Pivotal introduction</video>

### Different roles, different tasks, different responsibilities

Here's the roles we have on our teams:

*   Team Lead
*   Developer
*   Designer

Everyone on the team is required to participate, and is asked to pay attention to a few ironclad rules:

*   You can define stories, but you need to always comply to the "As a ..., I should be able to ..." description style and place your new stories in the icebox for the Team Lead to review.
*   Only the Team Lead can prioritize stories (by dragging them to the backlog/current), if you need to prioritize dependencies first add your requirement as blockers to a story (Pivotal feature).
*   Try to work at ONE STORY AT A TIME - and always the top-most one. If you need to work on multiple stories at once, it's a smell (meaning planning was not done well enough) and you must warn the Tem Lead.
*   You are welcome to break down a story into smaller ones or use the tasks inside a story to describe the sub-tasks needed to finish a story.

### The life-cycle of a User Story

Here's a quick sketch of how the life-cycle of a story looks: ![Story life-cycle](http://content.screencast.com/users/jeppeliisberg/folders/Jing/media/f342f0c3-afb3-44e7-8760-4d4543af7228/00000226.png)

### A note on discussions and team communications

Many people use e-mail as the primary way of communication. But e-mail is bad. Way too often, threads are broken, the body drifts from the subject (if a proper subject was there from the start) and either too many or too few are in on the 'cc' list.

We prefer chat over e-mail. Our chat is used for short-lived discussions that lead to decisions and actions. Decisions is then documented elsewhere (eg. on the scrum board) and actions are taken by the relevant people.

Discussions that are related to a specific story, bug or chore (task), should always be documented in the relevant story on the scrum board. Either by having that conversation right there in the story, or by copying or writing down any relevant information from the chat (or even e-mail) into the story. Having all relevant information regarding a specific story in the story itself is crucial for the ability of developers to focus and efficiently deliver the right product!


## Commit guidelines

They way we work is heavily inspired from [The way the github team works](http://zachholman.com/talk/how-github-uses-github-to-build-github).

### Rules of engagement

1.  commit every single change separately
2.  always start a commit message with a short (50 chars or less) summary
3.  remember ticket/story reference (see [Pivotal guide](https://www.pivotaltracker.com/help/api#scm_post_commit))
4.  never use `git commit -m` - think it through and read it again before you commit

### Example commit message

    Capitalized, short (50 chars or less) summary

    More detailed explanatory text, if necessary.  Wrap it to about 72
    characters or so.  In some contexts, the first line is treated as the
    subject of an email and the rest of the text as the body.  The blank
    line separating the summary from the body is critical (unless you omit
    the body entirely); tools like rebase can get confused if you run the
    two together.

    Write your commit message in the present tense: "Fix bug" and not "Fixed
    bug."  This convention matches up with commit messages generated by
    commands like git merge and git revert.

    Further paragraphs come after blank lines.

    - Bullet points are okay, too

    - Typically a hyphen or asterisk is used for the bullet, preceded by a
      single space, with blank lines in between, but conventions vary here

    - Use a hanging indent

    [Completes #12345]

From [A Note About Git Commit Messages](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)

NOTE: The last line is the pivotal integration to link your commit to a related story.

### Some background/philosophy

> _Commit messages are important._ They document the project’s progress and they’re a great way to see what has been done in a commit without having to read the code. Also, commit messages make it easy to dive into git log and find that commit you want to review or revert.

From [Git your act together](http://jeffkreeftmeijer.com/2010/git-your-act-together/)

## Branches and pull requests

We work using the master branch, branching out for any change and merging back to master using pull requests

![branching and pull requests](http://content.screencast.com/users/jeppeliisberg/folders/Jing/media/e60b3b23-9943-44c7-ac9d-f11c831391c8/00000004.png "Branching and pull requests")

Here's a few iron clad rules:

*   Master is ALWAYS deployable
*   NEVER commit directly to master - always push a change branch and issue a pull request
*   At least one other person should review and approve or comment
*   When at least two people (including comitter) has approved the request, anyone is allowed to merge into master
*   When a pull request is merged, the person who merged must delete the corresponding branch from github
*   Add a description to the PR - refer to the related Pivotal stor(y/ies) and include your considerations about this specific implementation.
*   If your code changes the UI in any way, include screenshots in the description of the PR.

Here's a few rules of thumb:

*   Pull requests are cheap, don't be afraid to toss it away
*   Use pull requests to allow others to review and comment on ideas and experiements
*   Try to keep change branches and pull requests small and get them merged fast

## Common Questions

**Q: Where should I put my comment - in Pivotal or in the Pull request on Github?**

1. Everything that is discussed before there's a PR os in Pivotal
2. When a PR is present, the discussion should probably mostly stay in that. Pull requests are meant for code review, so discussions about the specific implementation and the code should live here.
3. If the reviews and discussions in a PR turns into more genral issues, for example about the underlying software design or architecture, that change the implementation away from the spec in the story, the story should be updated or amended with this updated information.
