## 5/5/26
## Setup

To attribute your commits, set your identity.
```bash
git config --global user.name "My Name"
```
```bash
git config --global user.email "myemail@car.rier"
```

To download a project, use
```bash
git clone <url>
```
- If you are not making any changes to the project, simply `rm -rf .git`
## Starting a Project

Initialize git and create an instance in a project directory
```
git init
```
```
git status
```

**untracked files** (??) - files not added into the project vesions

**added files** (A) - files recognized by Git in a project

**modified files** (M) - files that differ from the last project version 
- Use `git restore` to restore the last version

Add a new or modified file into the project.
```
git add
```

**.gitignore** - text file with a list of every file or type that isn't relevant for other people

Commit some changes.
```bash
git commit -m "my message"
```
```bash
git remote add origin <link>
```
```bash
git push -u origin <branch name>
```
```bash
git diff
```
```bash
git stash
```