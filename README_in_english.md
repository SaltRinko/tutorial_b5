# Question

## Preparation before question

1. Create git hub account.
2. Register git hub account on local working PC.
   ```git config --global user.name "account name"```  
   ```git config --global user.email "Mail address"```  
3. Create remote repository on git hub.
4. Create a working repository locally. (create working directory, move to it and execution ```git init```.)  
5. Registering a remote repository.
   ```git remote add origin <link of remote repository>```  
6. Create some files in the local repository and reflect them in the remote repository.  
   (Example)  
   ```touch test.txt (creation of some kind of file)```  
   ```git add .```  
   ```git commit - m "initial commit"```  
   ```git push origin master```  

### After that, each group, please do yourself!!  

## Basic level question  

### Conflict festival at Master Branch!!

Answer the question on the paper.
Complete the file reflecting the editing contents of all the members while resolving the conflict.

## Advanced level question

### Let's memorize various git commands!!

Q 0: Move from master branch to challenge branch  
Since the challenge branch has already been created, there is no need to create a new branch.  
(The following problems are also done with the challenge branch.)  
The challenge branch accumulates commits with various edits added to the users.csv file.  
Perform the following exercises using those commit logs.  
Tip: It is useful to use ```git log --graph``` to see the previous commit logs!!  

Question 1: Cancel the change from the latest commit to the commit of the commit message "佐藤さんの要望(Mr. Sato's request)" (The commitment of "佐藤さんの要望(Mr. Sato's request)" is left)  

Question 2: As it was still better to cancel the commit message until "森さんの要望(Mr. Mori's request)", return to that point (leave the commitment of "森さんの要望(Mr. Mori's request)")  

Question 3: Correct the commit message "森さんの要望(Mr. Mori's request)" to "林さんの要望(Mr. Hayashi's request)"  

Question 4: Cancel only the commit of the commit message "吉田さんの要望(Mr. Yoshida's request)"  
However, keep the log that the commit has been canceled  

Question 5: Make a commit message reflect only commitment of "加藤さんの要望(Mr. Kato's request)" on the master branch  
In the event of a conflict, prioritize the editing content on the challenge branch side  

Question 6: Make multiple commit messages "木村さんの要望(Mr. Kimura's request)" together and make it the commit message "木村さんの全要望(All requests of Mr. Kimura)"   
Also, located one before "佐藤さんの要望(Mr. Sato's request)"  

Question 7: Edit the contents of the commit summarized in question 6 as follows  
Edit contents: add 100 to the value of "木村 翼(Kimura Tsubasa)"  

Question 8: Merge to master while keeping the commit history on challenge branch  

### Good job today! Now you are a Git master!!  
