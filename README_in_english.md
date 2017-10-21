# Practice problem

## Preparation before exercise

1. Create git hub account
2. Register git hub account on local working PC
   ```git config --global user.name "account name"```  
   ```git config --global user.email "Mail address"```  
3. Create remote repository on git hub
4. Create a working repository locally (create working directory, move to it and git init)
5. Registering a remote repository
   ```git remote add origin <link of remote repository>```  
6. Create some files in the local repository and reflect them in the remote repository  
   (Example)  
   ```touch test.txt (creation of some kind of file)```  
   ```git add .```  
   ```git commit - m "initial commit"```  
   ```git push origin master```  

### After that, each group, please do yourself!

## Elementary level problem

### Conflict festival at Master Branch!!

Each separate editing content dealt to the members is edited on the local master branch and push if you can edit it  
Complete the file reflecting the editing contents of all the members while resolving the conflict

## Development problem

### Let's memorize various git commands!!

Q 0: Move from master branch to challenge branch  
Since the challenge branch has already been created, there is no need to create a new branch  
(The following problems are also done with the challenge branch)  
The challenge branch accumulates commits with various edits added to the users.csv file  
Perform the following exercises using those commit logs  
Tip: It is useful to use git log --graph to see the previous commit logs!!  

Question 1: Cancel the change from the latest commit to the commit of the commit message "Mr. Sato's request" (The commitment of "Mr. Sato's request" is left)  

Question 2: As it was still better to cancel the commit message until "Mr. Mori's request", return to that point (leave the commitment of "Mr. Mori's request")  

Question 3: Correct the commit message "Mr. Mori's request" to "Mr. Hayashi's request"  

Question 4: Cancel only the commit of the commit message "Mr. Yoshida's request"  
However, keep the log that the commit has been canceled  

Q5: Please reflect only the commit of "Commission message" requested by Mr. Kato on the master branch  
In the event of a conflict, prioritize the editing content on the challenge branch side  

Q 6: Make all the commits where the commit message is "Mr. Kimura's request" all together and make the commit message "All requests of Mr. Kimura"  
Also, the position of the commit put together is to be put together at the last "Request of Mr. Kimura" (located one before Mr. Sato's request)  

Question 7: Edit the contents of the commit summarized in question 6 as follows  
Edit contents: add 100 to the value of "Kimura Tsubasa"  

Q 8: Merge to master while keeping the commit history on challenge branch  

Good job today! Now you are a Git master!!  
