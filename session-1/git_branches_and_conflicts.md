# Code the Future </>

## Session 1: Branching & Merge Conflicts

### Content covered in this session

  - [Session 1: Branching & Merge Conflicts](#session-1-branching--merge-conflicts)
    - [Content covered in this session](#content-covered-in-this-session)
    - [Session goals](#session-goals)
    - [What is a branch?](#what-is-a-branch)
    - [Why use branches?](#why-use-branches)
    - [Create, switch, and merge branches](#create-switch-and-merge-branches)
  - [What is a merge conflict?](#what-is-a-merge-conflict)
- [Resolve conflicts in VS Code (beginner guide)](#resolve-conflicts-in-vs-code-beginner-guide)
    - [Open the conflicted file](#open-the-conflicted-file)
    - [Choose how to resolve](#choose-how-to-resolve)
    - [Clean up](#clean-up)
    - [Save, stage, commit](#save-stage-commit)
    - [Hands-on exercise: create & resolve a conflict](#hands-on-exercise-create--resolve-a-conflict)
    - [1. Set up a test repo](#1-set-up-a-test-repo)
    - [2. Create a feature branch and change the file](#2-create-a-feature-branch-and-change-the-file)
    - [3. Change the same line on main](#3-change-the-same-line-on-main)
    - [4. Merge and resolve](#4-merge-and-resolve)
    - [Resources](#resources)

---

### Session goals

- Understand what branches are and why we use them  
- Create and switch between branches locally  
- Merge changes and recognise what a merge conflict is  
- Resolve a conflict using **VS Code** confidently

---

### What is a branch?

A **branch** is a separate line of development, like a safe sandbox to work on changes without touching the main version of your project.  
The default branch is often called **main**.

---

### Why use branches?

- Build new features without breaking the main code
- Let multiple people work in parallel
- Experiment safely and review changes before they go live

---

### Create, switch, and merge branches

Create a branch:
```
git branch new-feature-branch-name
```

Switch to it:
```
git checkout new-feature-branch-name
# or, in newer Git:
# git switch new-feature-branch-name
```

Do your work (edit files, commit), then merge back into main:
```
git checkout main
git merge new-feature-branch-name
```
If Git can combine changes automatically, the merge just completes.
If not, you'll see a merge conflict (next section).

## What is a merge conflict?

A **merge conflict** happens when two branches change the **same part** of the **same file**.
Git can't decide which version is correct, so it asks you to choose.

Conflict markers look like this inside a file:
```
<<<<<<< HEAD
Your version (current branch)
=======
Their version (incoming branch)
>>>>>>> new-feature-branch-name
```

You'll remove these markers after deciding what to keep.

# Resolve conflicts in VS Code (beginner guide)

### Open the conflicted file
- In the **Source Control** panel (left sidebar, branch icon), look under **Merge Changes** and click the file.

### Choose how to resolve
At each conflict block, VS Code shows buttons:

- **Accept Current Change** - keeps your branch version  
- **Accept Incoming Change** - keeps the branch you're merging  
- **Accept Both Changes** - keeps both versions (you can edit them together)  
- **Compare Changes** - see a side-by-side diff

### Clean up
- VS Code removes conflict markers automatically when you choose an option.  
- Re-read the file to ensure it reads correctly (no duplicates, extra lines, etc.).

### Save, stage, commit
1. Save the file.  
2. Stage it in **Source Control**.  
3. Commit with a message such as:  

```
Resolve merge conflict in index.html
```


That’s it — your merge completes.

**Tip:** Use the *side-by-side diff* in VS Code to clearly see what changed on each side.

---

### Hands-on exercise: create & resolve a conflict

**Goal:** Practice causing a conflict on purpose, then resolve it in VS Code.

### 1. Set up a test repo

```
mkdir merge-conflict-practice
cd merge-conflict-practice
git init
echo "Hello from main branch" > hello.txt
git add hello.txt
git commit -m "Initial commit"
```

### 2. Create a feature branch and change the file

```
git checkout -b new-feature
```

Open `hello.txt` and change the text to:

```
Hello from the feature branch
```

Then:

```
git add hello.txt
git commit -m "Change greeting on feature branch"
```

### 3. Change the same line on main

```
git checkout main
```

Edit `hello.txt` to:

```
Hello from the main branch
```

Then:
```
git add hello.txt
git commit -m "Change greeting on main branch"
```

###  4. Merge and resolve
```
git merge new-feature
```

You'll get a conflict in `hello.txt`.
Open it in **VS Code** -> choose **Accept Both Changes** (or pick one), tidy the text, save, stage, and commit:
```
Resolve conflict in hello.txt
```

You've merged successfully!

---


**Cheat sheet**

- Create branch: `git branch <name>`

- Switch branch: `git checkout <name>` or `git switch <name>`

- Create & switch: `git checkout -b <name>`

- Merge into current: `git merge <other-branch>`

- Abort a merge (if stuck): `git merge --abort`

- Pull latest main before work: `git checkout main && git pull`

**Conflict choices in VS Code**

- _Accept Current_ - keep your version

- _Accept Incoming_ - keep their version

- _Accept Both_ - keep both, then edit

---

### Resources
<ul> 
<li>
<a style="pointer-events:all" href="https://git-scm.com/docs" target="_blank" title="Official Git docs">Official Git docs</a>
</li> 
<li>
<a style="pointer-events:all" href="https://code.visualstudio.com/docs/sourcecontrol/overview" target="_blank" title="VS Code Source Control">VS Code: Source Control</a>
</li> 
<li><a style="pointer-events:all" href="https://code.visualstudio.com/docs/editor/versioncontrol" target="_blank" title="VS Code & Git">VS Code & Git</a>
</li> 
<li>
<a style="pointer-events:all" href="https://www.atlassian.com/git/tutorials/using-branches" target="_blank" title="Git branching tutorial">Git branching tutorial</a>
</li> 
</ul>

<div style="width: 100%">
<a href='intro_to_github.md'><-- Previous section: GitHub Desktop</a>
<div align="right">
<a  href='../session-2/README.md'>Next section: Session 2 Introduction --></a></div>
</div>
