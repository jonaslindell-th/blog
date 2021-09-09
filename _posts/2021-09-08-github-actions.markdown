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
CI is a practice which facilitates merging code to the main branch or commiting code to your branch continuously. By introducing a CI pipeline in Github actions for example, a commit to your branch or merge attempt to the main branch (depending on what triggers you choose to use), triggers a series of automated steps. These steps may involve running the code build, unit tests, code analysis and more.

If a new branch were to pass all of the automated steps in the pipeline without any errors, a merge to the main branch is possible and may continue to the next stage e.g. deployment to the cloud. Should any of the steps fail, the development team may go through the error report, so that they may fix the issues and the merge attempt is prevented from progressing to any further stages.

As to describe this proccess, the pipeline acts as a safety net between commits that may "break" the application and a fully functional deployment.

### What benefits does CI bring to the table?

By aiming at merging to the main branch often and in short iterations, running automated builds and tests continously, developers can catch any errors early in the development stage. Reducing time spent trying to find and fix bugs as well as preventing them from reaching deployment.

### How I implemented a CI pipeline into a existing project

---

As a first step, a .github directory is needed in my repository, this is where all Github specific files should be located. In this directory I introduce a workflows directory, this directory should contain my yaml file, what I name this file apart from .yaml is not important.

Once I have my yaml file, I start off by naming my workflow, this will be displayed in my repository's actions page once I trigger the workflow.

```yaml
name: workflow demonstration
```

The next step is to add the "on:" event which specifies on what event github should trigger the workflow.

```yaml
name: workflow demonstration
on: [push]
```

Now I have to specify what jobs and steps to run once this event is triggered. In my case I choose to build the application and run my unit tests, I find: "Verify build and run tests" a suitable name for this job.

```yaml
name: workflow demonstration
on: [push]
jobs:
  build:
    name: Verify build and run tests
```

Next my workflow needs to know what virtual enviroment to use to run this is, in my case i prefer to use linux ubuntu since performence is slightly faster.

```yaml
name: workflow demonstration
on: [push]
jobs:
  build:
    name: Verify build and run tests
    runs-on: ubuntu-latest
```

### References

---

[semaphoreci-continuous-integration](https://semaphoreci.com/continuous-integration)
