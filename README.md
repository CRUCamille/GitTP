# A small collaboration project to practice git 
This is simple pcg solver in c++ generated by chatgpt and modified after. 

The objective of this TP is not to understand c++ code, but to practice git. 

salut 
In fact, in the program, lots of sections are commented in main.cpp. What you need to do is to remove "/*" before the section and "*/" after each section to let the program output information.

As there are several files, you can work in groupe (2 personnes) to achieve the efficiency. 
## 1. Fork the project
You do not have write permission on this project, you will hence need to fork it. Of course, since ***Dev.A*** and ***Dev.B*** will be collaborating to the same project, only one of them should create the fork for the group.

***Dev.B***: Fork the project by clicking on the fork button in the upper right corner of the project page.

Now ***Dev.B*** has his own copy of the project. In order to give ***Dev.A*** write permissions to the project,
***Dev.B*** needs to add ***Dev.A*** to the project’s list of collaborators: *Settings -> Collaborators*.

## 2. Clone the repository
Both ***Dev.A*** and ***Dev.B*** clone it and then go to the local repository 
```
cd GitTP
```
Both open gitk to visualize the workflow
```
gitk --all &
```
gitk should be updated after each git command to check the changes.
## 3. Commit and push
In this part, ***Dev.B*** does the same thing as ***Dev.A***, but in *Step 2*
1. ***Dev.A*** delete "/*" and "*/" in *Step 1* in file *main.cpp*, check the change with 
```
git statut
```
2. ***Dev.A*** stage the modifications (check gitk)
```
git add main.cpp
```
3. ***Dev.A*** commit this modifications 
```
git commit -m "uncomment Step 1"
```
check gitk

4. ***Dev.A*** push this commit
```
git push
```
> One of the teammate will find that it is not possible to push the modifications. Try to figure it out. 

> Tips: The teammate push after the first need to do ```git pull``` before the ```git push```

5. Try to get the same output for gitk when finished. 

## 4. Branch and merge
In this part, ***Dev.B*** does the same thing as ***Dev.A***, but in *Step 4*
1. ***Dev.A*** creates a branch "uncommentStep3" ("uncommentStep4" for ***Dev.B***)
2. Checkout to the new branch, and check it to make sure
```
git branch
```
3. ***Dev.A*** deletes comments of *Step 3*
4. Commit the modifications and merge it to main branch
```
git checkout main
git merge uncommentStep3
```
5. push it to remote and try to get the same workflow one gitk 

## 5. Manage conflicts 
1. ***Dev.B*** creates a new branch "PCG".
2. ***Dev.B*** uncomments *Step 6.1* and **delete** *Step 6.2*.
3. ***Dev.B*** commits this modification and merge it main. 
4. ***Dev.B*** publishes it to remote.
5. ***Dev.A*** creates a new branch "CG".
6. ***Dev.A*** uncomments *Step 6.2* and **delete** *Step 6.1*.
7. ***Dev.A*** commits this modification.
8. ***Dev.A*** checkout to main.
9. ***Dev.A*** does a git pull to update his local main branch
10. ***Dev.A*** merge branch "CG" to main.  
11. ***Dev.A*** publishes it to remote.

> Here ***Dev.A*** has to handle the conflicts when merge "CG" to main. You can choose either PCG or CG. 
