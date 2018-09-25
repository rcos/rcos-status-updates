# rcos-status-updates
A starter repository for RCOS student status updates.

## What are Status Updates?

Status Updates are informal weekly short-form blog posts detailing a student's progress in RCOS during the previous week. Please consult the [RCOS Handbook](https://handbook.rcos.io/#/grading/status_updates) for a detailed overview of background and requirements.


## System Requirements
- [Git](https://git-scm.com/)


## Submitting Status Updates

1. Write a new status update in the directory corresponding to the current semester (i.e. `summer_2018`). Please use [Markdown](https://en.wikipedia.org/wiki/Markdown) and name this file something like `week_01.md`.

2. Track and commit your changes:

```
git add .
git commit -m 'Added status update for week 01'
```

3. Push your status update to the `master` branch of your fork:

```
git push origin master
```

4. All done :)


## Beginning of Semseter Setup

**These steps are important - if you don't follow them correctly your status updates won't be recognized by our auto-grader.**

1. Fork this repository (`rcos/rcos-status-updates`) so you have your own copy hosted on GitHub at `github.com/your-username/rcos-status-updates`.

2. Clone your fork of the repository down to your local machine and navigate into the resulting directory:

```
git clone https://github.com/your-username/rcos-status-updates.git
cd rcos-status-updates
```

3. Make a new directory to store your status updates for the semester. This directory **must** use the `semester_year` naming convention, all lowercase. For example:

```
fall_2018
spring_2019
summer_2019
```

This repository comes with a starter directory for the current semester (`fall_2018`).

4. Setup is complete :)
