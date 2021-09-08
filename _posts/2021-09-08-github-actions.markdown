---
layout: post
title: "Github Actions"
date: 2021-09-08 20:15:00 +0200
categories: jekyll update
---

## Introduction to Github Actions, Continuous Integration (CI)

---

<br/><br/>

### What is a CI Pipeline?

---

<br/><br/>
CI is a practice which facilitates merging code to the master branch or commiting code to your branch continuously. By introducing a CI pipeline in Github actions for example, a code commit or merge attempt to the main branch (depending on what triggers you choose to use), triggers a series of automated steps. These steps may involve running the code build, unit tests, code analysis and more.

If a new code branch were to pass all of the automated steps in the pipeline without any errors, a merge to the main branch is possible and may continue to the next stage e.g. deployment to the cloud. Should any of the steps fail, a notification is sent to the development team containing the error report, so that they may fix the issues and the merge attempt is prevented from progressing to any further stages.

As to describe this proccess, the pipeline acts as a safety net between commits that may "break" the application and a fully functional deployment.

### What benefits does CI bring to the table?

### References

---

[semaphoreci-continuous-integration](https://semaphoreci.com/continuous-integration)
