# Git
---


## What is Git ?

**Git** is a *free* and *open-source* **version control system**, originally created by *Linus Torvalds* in 2005. Unlike older centralized version control systems such as *SVN* and *CVS*, **Git** is distributed: every developer has **the full history** of their code repository locally. This makes the initial clone of the repository slower, but subsequent operations such as `commit`, `blame`, `diff`, `merge`, and `log` dramatically faster.

**Git** also has excellent support for `branching`, `merging`, and `rewriting` repository history, which has led to many innovative and powerful workflows and tools. `Pull requests` are one such popular tool that allows teams to collaborate on *Git branches* and efficiently *review* each other's code. **Git** is the most widely used version control system in the world today and is considered the modern standard for software development.


---


## How Git works

Git saves Snapshots, **not differences**! Most other systems store information as a list of *file-based changes*. These other Systems think of the information they store as a set of files and the changes made to each file over time. 
Git doesn't think of or store its data this way. Instead, Git thinks of its data more like a **series of snapshots** of a *miniature filesystem*. With Git, every time you `commit`, or save the state of your project, Git basically takes a picture of what all your files look like at that moment and stores a reference to that **snapshot**. To be efficient, if files have **not** changed, Git doesn’t store the file again, just a link to the previous identical file it has already stored. 

> Git thinks about its data more like a **stream of snapshots**


Git has integrity. Everything in Git is checksummed before it is stored and is then referred to by that checksum. This means it’s impossible to change the contents of any file or directory without Git knowing about it. This functionality is built into Git at the lowest levels and is integral to its philosophy. You can’t lose information in transit or get file corruption without Git being able to detect it.

The mechanism that Git uses for this checksumming is called a *SHA-1 hash*. This is a 40-character string composed of hexadecimal characters (0–9 and a–f) and calculated based on the contents of a file or directory structure in Git. A *SHA-1 hash* looks something like this:

>24b9da6552252987aa493b52f8696cd6d3b00373



---


## Git Workflow

1. Create a **repository** (*project*) with a *git hosting tool* (like [[BitBucket]])
2. **Copy** (or *clone*) the **repository** to your local machine
3. Add a file to your local **repo** and `commit` (*save*) the changes
4. `Push` your changes to your **main branch**
5. Make a change to your file with a git hosting tool and `commit`
6. `Pull` the changes to your local machine
7. Create a **branch** (version), make a change, `commit` the change
8. Open a `pull request` (propose changes to the **main branch**)
9. `Merge` your **branch** to the **main branch**


---


## What is a branch?

A **branch** is nothing but a pointer to the latest commit in the Git repository.
### Why are multiple branches needed?
Multiple branches are needed to support **multiple parallel developments**. Refer the image below to see how branches work.

![[Branch Example.jpg]]

Initially, `commit 1` and `commit 2` were done in the *master branch*. After `commit 2` a new Branch called as “*Test*” is created, and `commit 3` and `commit 4` are added to the *test branch*.

At the same time, a different `commit 3` and `commit 4` are added to the *master branch*. Here we can see that after `commit 2`, **two parallel developments** are being done in **2 separate branches**.

The *Test Branch* and the *Master Branch* have diverged here and have different code — the code from `Test Branch` can be merged with the `Master branch` using `git merge`.





###### External Links:
---
[Getting Git right](https://www.atlassian.com/git)
[Git Cheatsheet](https://cs.fyi/guide/git-cheatsheet)
[W3 Git Tutorial](https://www.w3schools.com/git/)

---
