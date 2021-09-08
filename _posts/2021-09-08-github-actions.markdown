---
layout: post
title: "Github Actions"
date: 2021-09-08 20:15:00 +0200
categories: jekyll update
---

## Introduction to Github Actions, Continuous Integration (CI)

---

### What is a CI Pipeline?

---

CI is a practice which facilitates merging code to the master branch continuously. By introducing a CI pipeline in Github actions for example, a merge attempt to the main branch triggers a series of automated steps. These steps may involve running the code build, unit tests and code analysis. If all automated steps pass the pipeline, the merge to the main branch is successfull and may continue to the next stage e.g. deployment to the cloud. Should any of the steps fail, a notification is sent to the development team containing the error report, so that they may fix the issues and the merge attempt is prevented from progressing to any further stages.

### References

---

[semaphoreci-continuous-integration](https://semaphoreci.com/continuous-integration)