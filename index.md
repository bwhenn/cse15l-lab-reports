### Lab Report 1 
---

- `cd`
  1. No arguments
       When entering `cd` into the terminal from any location, nothing is printed and the working dicectory is not changed. This is the output recieved becasue the command is used to change the working directory, but no path was given. No error has occured because the terminal doesnt know which directory to change into.
![cd1](https://github.com/bwhenn/cse15l-lab-reports/blob/main/cd1.png)
  2. With directory path as an argument
    When entering `cd lecture1/` into the terminal from the home directory, nothing is printed but the working directory is changed to the location specified by the path. Because the user can check the working directory using another command, no output is needed.
  ![cd2](https://github.com/bwhenn/cse15l-lab-reports/blob/main/cd2.png)
  4. With file path as an argument
     When entering `cd lecture1/Hello.java` into the terminal, the error message "Not a directory" is printed. This is expected becasue working dicrectories cannot be files. Directories contain files and subdirectories.
![cd3](https://github.com/bwhenn/cse15l-lab-reports/blob/main/cd3.png) 
- `ls`
  1. No arguments
     When entering `ls` into the terminal, a list of the contents of the working directory is printed out. Because ls is short for list, we can expect this output from the command. For example, when you run this command in the "messages" directory, "en-us.txt", "es.mx.txt", and "zh.cn.txt" will be printed.
  ![ls1](https://github.com/bwhenn/cse15l-lab-reports/blob/main/ls1.png)
  3. With directory path as an argument
     When entering `ls lecture1/messages` from the home directory of the workspace, the contents of the messages directory are printed even though messages is not the current working directory. This shows that the contents of a directory can be listed even if it is not the working directory so long as a path is given to that location.
![ls2](https://github.com/bwhenn/cse15l-lab-reports/blob/main/ls2.png)
  3. With file path as an argument
     When entering `ls lecture1/messages/en-us.txt` is entered, the same file path name is returned. This is becasue the argument is no longer a dictory with contents enlosed to list. This means that we cannot go futher in the nested file structure, and because of this, there only the file path to be printed back.
![ls3](https://github.com/bwhenn/cse15l-lab-reports/blob/main/ls3.png)
- `cat`
  1. No arguments
      When entering `cat` from any directory with no arguments, the shell will not print anything and enter an input mode until Ctrl-D is pressed, effectively exiting the command call. This command is used to quickly display the context of text-based files to the terminal. Therefore, we see this unexpected behavior because no file paths have been provided.
  ![cat1](https://github.com/bwhenn/cse15l-lab-reports/blob/main/cat1.png)
  2. With directory path as an argument
     When entering `cat lecture1/` from the home directory, the error message "Is a directory" is printed back to the terminal. This can be expected because cat is meant to display file contents, and not directory contents. `ls` should be used to list the contents of a directory.
![cat2](https://github.com/bwhenn/cse15l-lab-reports/blob/main/cat2.png)
  3. With file path as an argument
     When entering `cat lecture1/messages/en-us.txt` from the home directory, all the contents of the file specified by the path are printed (A single line containing "Hello World!"). This is the expected output for any text based file. However, when passing a non-text based file, such as the binary file Hello.class, the output printed by cat is nonsensicle and cannot be interpreted.
  ![cat3](https://github.com/bwhenn/cse15l-lab-reports/blob/main/cat3.png)
