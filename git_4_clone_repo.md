# Clone a Repository
---
**Q:  What is cloning?**  
**A:  Making a copy of something.**

![orphan black](images/orphan_black.jpg)

---

## Select green button "Clone or download" and copy url

### Go to directory on local computer  
For me, it is: `/Users/florianmoss/ds/gitsample`  
>my example
```bash
pwd
/Users/florianmoss/ds/gitsample
```

#### Clone repo
`git clone https://github.com/florianmoss/starting_git.git`  


### `cd` into cloned repo
<kbd> ls </kbd>  
<kbd> cd starting_git </kbd>
<kbd> ls </kbd>  
<kbd> pwd </kbd>  

## Check out the remote
**Remotes** are copies of a repo on another computer **(or on a service like Github)**  

**Example:**  
* `upstream` [organization repo]
* `origin`   [your forked repo]

**Note:**  
* notice you have push and pull access  

>my example  
```bash
▶ git remote -v
origin	https://github.com/florianmoss/starting_git.git (fetch)
origin	https://github.com/florianmoss/starting_git.git (push)
```

### We can 'pull' updates from GitHub version
```bash
▶ git pull
Already up-to-date.
```

## Make changes on local computer 

### Let's make a change on local computer and push changes up to GitHub
Use an editor of your choice to create a java file which will print your name.  
My file `print_name.java` contains the following line of code:  
```java
System.out.print("My name is Florian")
```

## We made a change!  How does git track it? `git status`
To see what changes have been made since last `git pull`, type `git status`  
```bash
▶ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	print_name.java

nothing added to commit but untracked files present (use "git add" to track)

```
---

## Next up:  how do we send those changes up to GitHub? :boom:


