# Workflow 2:  Submit Pull Request, Steps A to Z

## Step 1:  fork the repo (on GitHub)
https://github.com/florianmoss/learn-oop-java

## Step 2:  copy forked url for cloning 
<img src="../images/github_clone_button.png" align="left" height="40" width="60" >    
Click on the green button for your forked GitHub repo, and ensure it is showing the url for "Clone with HTTPS"  (other option is "Clone with SSH").  Copy that URL.    


  
    
    
>my example  
```text
https://github.com/florianmoss/learn-oop-java.git
```

## Step 3:  go to working directory (your local terminal)
Go to your working directory  
>my example
```bash
cd /Users/florianmoss/ds/gitsample
```

## Step 4:  clone the repo  
<kbd> git clone <url> </kbd> 
>my example
```bash
git clone https://github.com/florianmoss/learn-oop-java.git
```

## Step 5:  `cd` into the repo
<kbd> cd <repo_name> </kbd>
>my example
```bash
cd learn-oop-java
```

## Step 6:  look at remotes
<kbd> git remote -v </kbd>
>my example
```bash
origin	https://github.com/florianmoss/learn-oop-java.git (fetch)
origin	https://github.com/florianmoss/learn-oop-java.git (push)
```

## Step 7:  add 'upstream' remote
<kbd> git remote add upstream <url> </kbd>
>my example
```bash
git remote add upstream https://github.com/florianmoss/learn-oop-java.git
```

## Step 8:  look at remotes
<kbd> git remote -v </kbd>  
>my example
```bash
origin	https://github.com/florianmoss/learn-oop-java (fetch)
origin	https://github.com/florianmoss/learn-oop-java (push)
upstream	https://github.com/florianmoss/learn-oop-java (fetch)
upstream	https://github.com/florianmoss/learn-oop-java (push)
```

## Step 9:  update a repo
This step copies changes from a remote repository to a local repository.  
**Note:**  this is a good step to practice even though the first time you clone a repo it will already be up to date.   

<kbd> git pull </kbd>  
or a more complete syntax to use is:  
<kbd> git pull upstream master </kbd>  

## Step 10:  list branches
<kbd> git branch </kbd>  
>my example
```git
git branch
* master
```
 
## Step 11:  create a working branch
<kbd> git branch <branch_name> </kbd>
>my example  
`git branch florian_wip`

## Step 12:  list branches
<kbd> git branch </kbd>  
>my example
```git
git branch
* master
  florian_wip
```

## Step 13:  switch to working branch
<kbd> git checkout <branch_name> </kbd>  
>my example  
`git checkout florian_wip`

## Step 14:  create a file
Note:  We will submit a pull request to the repo and that file will go here:  https://github.com/florianmoss/learn-oop-java/tree/master/submissions  

- create a folder in the repo with your name here:  `learn-oop-java/submissions`
- `cd` into this folder, create a folder with your name
- create a Java file (Example:  `test_java_file.java`)

<kbd> pwd </kbd>  
<kbd> ls </kbd>  
<kbd> cd submissions </kbd>  
<kbd> mkdir florian </kbd>  
<kbd>  cd florian </kbd>  
<kbd>  touch test_java_file.java </kbd>  

>my example
```bash
% pwd
/Users/florianmoss/ds/gitsample/learn-oop-java
% cd submissions 
% mkdir florian
% cd florian
% touch test_java_file.java
```
    
## Step 15:  add/stage a file
<kbd> git add <file_name> </kbd>  
>my example  
`git add test_java_file.java`

## Step 16:  commit a file
<kbd> git commit -m 'message' </kbd>
>my example
 `git commit -m 'adding my java test file`
 
## Step 17:  push changes to your 'working branch'
<kbd> git push origin <branch_wip> </kbd>  
>my example
`git push origin florian_wip`

## Step 18 (optional):  copy changes over to master branch
We'll submit the pull request from the `master` branch.  
1. Switch to master branch  
<kbd> git checkout master </kbd>  
2. Copy file over to master branch  
<kbd> git checkout florian_wip florian/venus.java </kbd>  
3. **A**dd / **C**ommit / **P**ush the file to master branch
```bash
% pwd
/Users/florianmoss/ds/gitsample/learn-oop-java/submissions
ls florian
git checkout master
git checkout florian_wip florian/venus.java
git status
git add florian/venus.java
git status
git commit -m ' adding venus file to master branch'
git status
git push origin master
``` 


## Step 19:  submit pull request (on GitHub)

Select green button "Compare and pull request"  
<img src="../images/pull_request_button.png" align="left" height="40" width="180" >   <br> <br>

---

## Summary of Steps
<kbd> cd /Users/florianmoss/ds/gitsample </kbd>  
<kbd> pwd </kbd>   
<kbd> git clone https://github.com/florianmoss/learn-oop-java.git </kbd>  
<kbd> cd learn-oop-java </kbd>   
<kbd> git remote -v </kbd>  
<kbd> git remote add upstream https://github.com/florianmoss/learn-oop-java.git </kbd>  
<kbd> git remote -v </kbd>  
<kbd> git pull </kbd>  or <kbd> git pull upstream master </kbd>  
<kbd> git branch </kbd> <kbd> git branch florian_wip </kbd>  
<kbd> git branch </kbd> <kbd> git checkout florian_wip </kbd>  
<kbd> cd submissions </kbd>  
<kbd> mkdir florian </kbd>  
<kbd>  cd florian </kbd>  
<kbd>  touch test_java_file.java </kbd>  
<kbd>  ls </kbd>  
<kbd>  git status </kbd> <kbd>  git add test_java_file.java  </kbd>  		  
<kbd>  git status </kbd> <kbd>  git commit -m 'adding my java test file' </kbd>  		  
<kbd>  git status </kbd> <kbd>  git push origin florian_wip </kbd> 
