# rcos-status-updates
A starter repository for RCOS student status updates.

## What are Status Updates?

Status Updates are informal weekly short-form blog posts detailing a student's progress in RCOS during the previous week. Please consult the [RCOS Handbook](https://handbook.rcos.io/#/grading/status_updates) for a detailed overview of background and requirements.

## System Requirements
- [Git](https://git-scm.com/)

## First-Time Setup

**If you're a first-time RCOS student follow these steps to get started:**

1. Fork this repository (`rcos/rcos-status-updates`) so you have your own copy.

2. Clone the your fork of this repository down to your local machine and navigate into the resulting directory:

```
git clone https://github.com/your-username/rcos-status-updates.git
cd rcos-status-updates
```

3. Copy the `.new_semester` template directory to store your status updates for the semester. This directory **must** use the `year_semester` naming convention, all lowercase. For example:

```
2018_summer
2018_fall
2019_spring
```

You can copy the `.new_semester` directory with the following command:

```
cp -R .new_semester 2018_summer
```

4. First-time setup is complete :)


## Returning Student Setup

**If you're a returning RCOS student follow these steps at the beginning of the semester:**

1. Navigate to your local copy of this repository, for example:

```
cd ~/code/rcos-status-updates
```

Make sure that all your current changes have been saved and committed - you can check with the `git status` command.

2. Copy the `.new_semester` template directory to store your status updates for the semester. This directory **must** use the `year_semester` naming convention, all lowercase. For example:

```
2018_summer
2018_fall
2019_spring
```

You can copy the `.new_semester` directory with the following command:

```
cp -R .new_semester 2018_summer
```


3. Returning student setup is complete :)


## Submitting Status Updates

1. Write a new status update in the directory corresponding to the current semester (i.e. `summer_2018`).

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