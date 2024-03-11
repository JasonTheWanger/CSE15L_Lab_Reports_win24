Lab Report 5
============

__Student__: Hi there, I am encountering a coding bug in my lab6 list example grading script. I am on a unix based system and run the following command `junranwang@oushunzens-MacBook-Pro Lab6_list-examples-grader % bash grade.sh https://github.com/ucsd-cse15l-f22/list-methods-lab3 ` in VS_Code. I was expecting to get all success outputs from the junit test but it failed one of the test somehow. I will have my code, junit test, junit test result, and my bash script attached below. Can someone help me to explain what is/are the issue with my code? What are the possible ways to address my issue?

![Image](Student_Code.png)
![Image](Tester.png)
![Image](Junit_Result.png)
![Image](Bash.png)

__TA__: Looking at your evidence document, your junit tester and bash script are done correctly. However, the reason why you are getting such test failure output is because your program timedout, possibly due to encountering a infinite loop. Double check your loops, check if your conditional variable is being updated accordingly in your ListExamples.java.

__Student__: Thanks for the hint, I've succeessfully found the bug in my code. The bug was cause by the infinity while loop when I was trying to merge the element in the second list into the result list. So I went to the repository that I git cloned from and made an update on the _ListExamples.java_ file I updated the wrong variable, index1, instead, I should update index2 since this variable is the conditional variable for this while loop. I fixed this bug in my code and passed the Junit test.

![Image](JunitSuccess.png)
![Image](UpdatedCode.png)

I am really appreciating the `vim` command. I never thought I can make a use of it outside the class!. There was once I have to edit some codes and submit my PA for cse12 on gradescope but I dont have my own computer. I borrowed my friend's computer but he doesn't have an ide installed. So I start cloning my code from github and using `vim` in the terminal to edit the java file, run junit test in the terminal as well, then push the updated file back to my github using the terminal. In the end, I successfully submitted the PA on time. This is my own experience of only using the terminal to make edits. I think it is very cool and super helpful. 
