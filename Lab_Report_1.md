`cd` command with no argument
=============================

Current directory is /lecture1

    [user@sahara ~/lecture1]$ cd
    [user@sahara ~]$

Current directory is /home

    [user@sahara ~]$ cd
    [user@sahara ~]$

Current directory is /lecture1/messages

    [user@sahara ~/lecture1/messages]$ cd
    [user@sahara ~]$

I simulated 3 different situation when using cd with no arguments. First case is when the working directory is /lecture1, second is when the directory is /home, and third is when the directory is /lecture1/messages.
If the current working directory is /home then nothing happens. If current working directory is /lecture1, current directory returns to /home. If the current directory is /lecture1/messages, current directory returns to /home. No error occured in these 3 cases with cd no arguments. No errors.

`cd` command with directory argument
=====================================

Current directory is /home

    [user@sahara ~]$ cd lecture1
    [user@sahara ~/lecture1]$

    [user@sahara ~]$ cd lecture2
    bash: cd: home: No such file or directory
    [user@sahara ~]$

By entering a directory as an argument after the cd command, the current working direcotry will be changed to the entered direcotry if it exists in the current directory. If the input directory does not exist in the current direcotry, the terminal will tell the user "No such file or directory".

`cd` command with file argument
================================

Current direcotry is /home/lecture1/messages

    [user@sahara ~/lecture1/messages]$ cd en-us.txt
    bash: cd: en-us.txt: Not a directory
    [user@sahara ~/lecture1/messages]$

If the argument is a file, for example, a text file, the ternimal will say the txt file is not a directory; therefore, it can not change the current directory to the txt file.

`ls` command with no argument 
===============================

Current directory is /home/lecture1/messages

    [user@sahara ~/lecture1/messages]$ ls
    en-us.txt  es-mx.txt  zh-cn.txt  zh-hk.txt

After entering the command of ls, the terminal will print out a list of all of the directories or files that is located in the current directory.

`ls` command with directory argument
====================================

Current directory is /home

    [user@sahara ~]$ ls lecture1
    Hello.class  Hello.java  messages  README

Current directory is /home

    [user@sahara ~]$ ls lecture1/messages
    en-us.txt  es-mx.txt  zh-cn.txt  zh-hk.txt

By entering the ls command with a argument of a directory, the terminal will show a list of all the directories or files in the input directory argument. 

`ls` commnad with file argument
=================================

Current direcotry is /home

    [user@sahara ~]$ ls lecture1/messages/en-us.txt
    lecture1/messages/en-us.txt

If the input argument is a file, the terminal will print out the relative path of the file location

`cat` command with no argument
===============================

Current directory is /home

    [user@sahara ~]$ cat
    /   
    /
    ~
    ~
If using cat command with no argument, the ternimal will read from standard input, then output what user has input in the terminal

`cat` command with directory argument
======================================

Current directory is /home

    [user@sahara ~]$ cat lecture1
    cat: lecture1: Is a directory

If the arugment is a direcotry, the ternimal will inform user that the input is a directory, not a file, where cat cannot provide a standard output.

`cat` command with file argument
=================================

Current direcotry is /home

    [user@sahara ~]$ cat lecture1/Hello.java
    import java.io.IOException;
    import java.nio.charset.StandardCharsets;
    import java.nio.file.Files;
    import java.nio.file.Path;
    
    public class Hello {
      public static void main(String[] args) throws IOException {
        String content = Files.readString(Path.of(args[0]), StandardCharsets.UTF_8);    
        System.out.println(content);
      }
    }
    [user@sahara ~]$ cat lecture1/messages/en-us.txt
    Hello World!
    [user@sahara ~]$ 

By entering a file argument after the cat command, the terminal will write the file to standard output of what is contained in the input file, such as, .java or .txt files.

    





    


