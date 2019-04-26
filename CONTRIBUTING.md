# Contribution Guide

To make sure your project follows APPI's contribution rules, please read the following guidelines.

## Branches naming convention

### TLDR

- Use tokens (words) at the beginning of your branch names.
- Define and use short lead tokens to differentiate branches in a way that is meaningful to your workflow.
- Use slashes to separate parts of your branch names.
- Do not use bare numbers as leading parts.
- Avoid long descriptive names for long-lived branches.
  Group tokens

### Tokens

Use one of the following tokens in front of your branch names to group it without a given category.

- `wip/`: Works in progress; stuff you know won't be finished soon
- `feat/`: Feature you're adding or expanding
- `bug/`: Bug fix
- `junk/`: trash branch created to experiment

### Do not use bare numbers

Do not use use bare numbers (or hex numbers) as part of your branch naming scheme. Inside tab-expansion of a reference name, git may decide that a number is part of a sha-1 instead of a branch name.

### Avoid long descriptive names

Long branch names can be very helpful when you are looking at a list of branches. But it can get in the way when looking at decorated one-line logs as the branch names can eat up most of the single line and abbreviate the visible part of the log.

## Commit convention

Each time you finished a part of your code which deserves to be described, you have to create a commit. In order to correctly write your commit message, use the following template.

```
Short description.
Added:
-
Modified:
-
Fixed:
-
Removed:
-
```

Between each part, you will describe what you've done. For example, if I've added a new route to the API, deleted a file named `useless.js` and fixed an existing bug (written in an issue), I will write the following commit message.

```
Route to add new customer
Added:
- New route to add a customer in the database
Fixed:
- Bug #14
Removed:
- file named 'useless.js' which is not relevant anymore
```

As you may have seen, in the `Fixed` part, you should always refer to an issue which is describing the bug. Furthermore, you have to separate your contributions using `-` on a new line. Finally, an empty section can be omitted.

## Merge request submission

A merge request should always be describe as follows.

```markdown
# Changelog

- Change 1 description
- Change 2 description
  ...
```

## Issue submission

An issue should always follow the template below.

```markdown
# As a

# I want

# So that

# Possible approaches (optional)

# Restrictions (optional)

# Conditions of satisfactions (optional)
```

## How to contribute?

- First, create a new branch (based on `dev`) with the correct token corresponding to your current task (remember naming conventions). For example, let say you want to add a new feature.

1. Go in the project directory you are working on.

```bash
cd /path/to/project
```

2. Get the latest version of `dev` branch.

```bash
git checkout dev
```

3. Create a new branch with the correct token.

```bash
git checkout -b feat/new-feature
```

4. Push your newly created branch on the remote git.

```bash
git push origin feat/new-feature
```

5. Create a merge request from `feat/new-feature` to `dev` with the `WIP` status (an URL should be given when you push your new branch on the remote git).

- Then, develop the stuff you need and remember to commit every time you add a new mechanism to your code which deserves to be described.

- Finally, once you've finished your task and written all your tests, remove the `WIP` status from your merge request and wait for the approval of your approvers.
