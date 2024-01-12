    [user@sahara ~/lecture1]$ cd
    [user@sahara ~]$
Current directory is /lecture1
---------------------------------
    [user@sahara ~]$ cd
    [user@sahara ~]$
Current directory is /home
---------------------------------
    [user@sahara ~/lecture1/messages]$ cd
    [user@sahara ~]$
Current directory is /lecture1/messages
---------------------------------
I simulated 3 different situation when using cd with no arguments. First case is when the working directory is /lecture1, second is when the directory is /home, and third is when the directory is /lecture1/messages.
If the current working directory is /home then nothing happens. If current working directory is /lecture1, current directory returns to /home. If the current directory is /lecture1/messages, current directory returns to /home. No error occured in these 3 cases with cd no arguments.


