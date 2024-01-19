Creating a good pull request could be hard. So this guide should help you do the first steps of creating a good, meaningful pull request.
You should always keep in mind, that this guide is only a suggestion and parts can be different in your project or need to be adjusted to work best for you and your team.

> Disclaimer: This guide is written by Aaron Czichon. It includes experiences and practices which works good in his projects. This is a guide to make developers more aware of good PR. Some points may differ for you, your team and your project.

## What's the goal of a pull request?

Pull requests should help to ensure the overall quality of your code which you want to merge into the project.
It helps you to get feedback on you implementations or changes. It shows also your team members what you have done and, more important, why you have done something.
It's important that the reviewing team members understand the changes and how they can test them and what these changes are affecting.
Let's divide the following sections on these needs: What has changed, why it has been changed how can they been tested.

## What has changed

Describe precisely what you have changed. Yes, your team members will check the code which has changed, but often it's hard to get into the changes as someone who has not written the code. 
Describe the most important parts from what you have changed to the new logic and which problems you have faced or why you have made some decisions. It's important that everyone understands your changes.

## Why it has been changed

More important than what has changed is the **why** something has changed. You can describe it inside the PR and even more important is that you link all your issues (tasks, user stories, work items, bugs, etc.). 
This enables the reviewer to check what was the initial need to the change inside the code. If the change request comes from a PO he can clarify with him/her directly parts he or she doesn't understand.

## How can the changes be tested

To keep the effort and time consumption low for the reviewers provide a detailed step-by-step guide on how the changes can be tested. 
If you need data to test the changes of the PR, provide testing data. Here now also start a bit the use case of the PR. If you're providing changes for the frontend, it's important to show visual changes and how the reviewers can test them.
If your changes includes changes on the backend, you may want to include a curl request or Postman collection on how they can be tested. 
The more information a reviewer gets, the faster and easier the pull request can be reviewed.

# Define a PR template

To help you getting started with a good PR, I defined a PR template which can be used and adjusted for your needs.

```markdown
# PR checklist

- [ ] Linked all relevant issues / work items
- [ ] Tested functionality locally (and PR deployment if available)
- [ ] Provided screenshots of all optical changes (frontend only)
- [ ] Updated `CHANGELOG.md`
- [ ] PR template filled completly
- [ ] Reviewer: Checked reviewer checklist

# General description

<!-- Describe why you have done these changes and what they do now. -->

# Changelog

<!-- 
The parts of the changelog this PR is responsible for. 
You can use this section to be auto-filled by e.g. commit messages if you stick to conventional commits. Here is an example:

## Features
- [🚀] Added new feature X

## Improvements
- [💎] Improved CI tasks
- [💎] Changed behavior of Y to Z

## Removals
- [🔥] Removed unused code in G

## Fixes
- [🐛] Fixed bug XYZ
-->
  

# What kind of changes are included

<!-- 
Include the kind of your change. This is important if you stick to 
semantic versioning.
-->
- [ ] Breaking API changes (Major version change)
- [ ] New features and fixes (Minor version change)
- [ ] Bugfixes only (Patch version change)

# Screenshots

<!-- 
If you have made optical and visual changes, please attach screenshots in this section.
Provide screenshots **before** and **after** your changes so the reviewer can get a clear view on the changes.
-->

# Testing instructions

<!--
Add a step-by-step guide on how these changes can be tested and what local setup is required.
-->

# Additional Information

<!-- If there is anything else, feel free to add it here. -->

# Responsible Developers

<!-- If these changes are made by more than one developer, please add the responsible person here. -->

# Affected modules/services/API/etc.

<!-- If your changes affecting any other service, library, API or anything else please add it here so somebody can take care of it. -->

# Reviewer checklist

<!-- This checklist is for the reviewer to make sure he or she doesn't forget anything. -->
- [ ] Changes are working as expected locally and, if available, on PR deployment
- [ ] Documentation is provided
- [ ] Tests are written / updated
- [ ] Code follows architectural approach of the team
- [ ] Changelog is updated correctly
```
