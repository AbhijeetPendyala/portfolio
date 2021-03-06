---
layout: post
title:  "Quick GIT commands"
date:   2017-06-19
desc: "Go to commands"
keywords: "GCP, Commandline, SSH"
categories: [GCP]
tags: [GCP,SSH]
icon: icon-html
---

<ul>
    <li> list all branches </li>  
</ul>

```
git branch –a

```
<ul>
    <li> checkout the branch you want to use  </li>  
</ul>

```
git checkout <feature_branch>

```
<ul>
    <li> confirm the branch you are working on  </li>  
</ul>

```
git branch 

```

<ul>
    <li> Initialize a repo </li>  
</ul>

```
git init 

```

<ul>
    <li> Adds the files in the local repository and stages them for commit, 
        To stage specific file, use its filename </li>  
</ul>

```
git add .

```

<ul>
    <li>  To unstage a file </li>  
</ul>

```
git reset HEAD your-file

```

<ul>
    <li> To commit a change </li>  
</ul>

```
git commit -m

```

<ul>
    <li> To remove a previous commit . Git reset is opposite of gid add
     --soft flag will preserve changes and just removes the commit</li>  
</ul>

```
git reset --soft HEAD~1

```

<ul>
    <li> To remove a commit and also undo changes.</li>  
</ul>

```
git reset --soft HEAD~1

```


<ul>
    <li> To revert back changes on a uncommited file (permanently) </li>  
</ul>

```
git checkout -- <file>

```

<ul>
    <li> Discard all local changes to all files permanently </li>  
</ul>

```
git reset --hard

```

<ul>
    <li> Check concise commit history </li>  
</ul>

```
git log --oneline --graph 

```

<ul>
    <li> list all branches </li>  
</ul>

```
git branch –a

```

<ul>
    <li>Add the URL for the remote repository where your local repository will be pushed </li>  
</ul>

```
 git remote add origin <remote repository URL>

```

<ul>
    <li> check remote status </li>  
</ul>

```
git remote -v

```

<ul>
    <li> Change remote (from old repo eg: previous company) to a new github repo ( first create a new repo and use its ssh link) </li>  
</ul>

```
git remote set-url origin git@github.com:username/repo.git

```

<ul>
    <li> To remove files from working tree and from index </li>  
</ul>

```
git rm --cached <file-name>

```

<ul>
    <li> To delete a local branch </li>  
</ul>

```
git branch -D <branch-name>

```

<ul>
    <li> To delete a remote branch </li>  
</ul>

```
git push origin --delete <branch-name>

```

<ul>
    <li> git checkout to a new branch </li>  
</ul>

```
git checkout -b <branch-name>

```

<ul>
    <li> Push the  new_name local branch and reset the upstream branch </li>  
</ul>

```
git push origin -u new_name

```
<ul>
    <li> to do dummy commit </li>  
</ul>

```
git commit --allow-empty -m "message"

```

<ul>
    <li> Histroy log in console </li>  
</ul>

```
git  log --all --decorate --online --graph

```


<ul>
    <li> Remember credentials for 1 hour (3600 seconds):</li>  
</ul>

```
git config --global credential.helper 'cache --timeout=3600' 

```

<ul>
    <li> Disabling cache</li>
</ul>

```
git config --global --unset credential.helper

``` 
<ul>
    <li> Export a repo as a an archive without .git </li>
</ul>

```
git archive --prefix= ADDITIONAL_PREFIX_INSIDE_ARCHIVE BRANCH_NAME -o OUTPUT_FILE.zip

``` 
---


<ul>
    <li> Duplicate a repository without forking it </li>  
</ul>

```

git clone --bare https://github.com/user/sample.git
cd sample.git
git push --mirror https://github.com/user/newrepo.git

```