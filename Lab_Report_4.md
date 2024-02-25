Lab Repot 4 - Vim
=================
Steps 4
-------
![Image](Login.png)

Key pressed: ``` ssh juw070@ieng6.ucsd.edu ```
***

Steps 5
-------
![Image](copySSHFromGitHub.png)

Copy the SSH url by clicking the copy icon
***

![Image](git_clone.png)

Key pressed: ``` git clone <command>v  ``` --> ``` git clone git@github.com:JasonTheWanger/lab7.git ``` I copy the path of the ssh url from my github account then typed ``` git clone ``` and pasted the url after the command.
***

Steps 6
-------
![Image](cd_lab7.png)

Key pressed: ``` cd lab7 ```
***

![Image](javac.png)

Key pressed: ``` javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java ```
***

![Image](java.png)

Key pressed: ``` java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests```
***

Steps 7
-------
![Image](vim.png)

Key pressed: ``` vim ListEamples.java ```
***

![Image](vim-fix.png)

Key pressed: ``` 43j e r2 ```
***

![Image](vim-quit.png)

Key pressed: ``` :wq! <enter> ```
***

Steps 8
-------
![Image](javac_after.png)

Key pressed: ``` <up> <up> <up> <enter> ``` --> ``` javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java ``` The javac command was in the history of the terminal so I typed 3 ```<up>``` key to access the command in the history.
***

![Image](java_after.png)
Key pressed: ``` <up> <up> <up> <enter> ``` --> ``` java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests ``` The java command was in the history of the terminal so I typed 3 ```<up>``` key to access the command in the history.
***

Steps 9
-------
![Image](git_add.png)

Key pressed: ``` git add "ListExamples.java" ```
***

![Image](git_commit.png)

Key pressed: ``` git commit -m "ListExamples.java" ```
***

![Image](git_push.png)

Key pressed: ``` git push -u origin main ```
***
