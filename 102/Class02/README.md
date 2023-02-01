## Class 2 Reading Notes
### Choosing a Text Editor
____
#### Text Editor Basics
- A __text editor__ allows you to write and manage text; especially text that you write to build website.  

- the software can be accessed online or downloaded and installed on your computer.  

- A good text editor will have the following features:  
    - code completion - closingbrackets, tags, and quaotations marks when you open them
    - syntax highlighting -  colorizing differnt parts of code
    - variety of themes - reduces eye stain and fatigue  
    - variety of __extentions__ readily availible- extenions are like plugins for your text editor; adds functionality
    - some third party options that offer some if not all of these features:
        - Notepad++
        - Text Wrangler
        - BB Edit
        - Visual Studio Code
        - Atom
        - Brackets
        - Sublime Text
- Every computer  comes with a _bare bones_ text editor
- Things to note when using preloaded text editor  
    - use plain text editor
    - save files with appropriate extention  
    - save those files to designated folder/subfolder  
#### The Command Line (Terminal)
- A **command line** aka **terminal** is a text based interface to the system
- A __shell__ is a part of the operating system that defines how the terminal behaves; *bash* is a common shell
- you can use the following command to display system variable stating your current shell  
    - ```  
         user@bash: echo $Shell  
         /bin/bash  
         user@bash:
    ```
- **Echo** is a command used to display messages
- To remotely open a terminal on Windows  you will need an SSH client i.e, *Putty*
#### Navigation
**_Location_**  
- A lot of commands on the terminal rely on location. To help keep track of where you are you can use commands like **PWD (Print Working Directory)** that will display what your current or present _working directory_ is
- use command **ls (list)** for a plain listing of what is in your current location  
    - ```
        user@bash: ls  
        bin Document public_html  
        user@bash:  
        ```
- We can run more powerful command by adding an options or arguments like (-l) to render a long list or (/etc) to render a list of the current directory's content  

**_Paths_**  
- The file system in Linux is a heirarchial structure begining with a root directory (denoted by a *single slash*)
    - root directory > subdirectory > files
- A **path** refers to a file or directory on the command line; it is a means to get to a particular file or directory on the system
    - *Absolute Path* specify a location in relation to the root directory; they begin with a forward slash:   ``` 
    ls  /home/ryan/Documents ```
    - *Relative Path* specify a location in ralation to where we currently are in the system: **_do not_** begin with a slash:   ``` 
    ls Documents ```  
- Some building blocks for your paths
    - ~ (tilde) - a shortcut for your home directory
    - . (dot) - a reference for your current directory
    - .. (dotdot) - a reference to the parent directory   
- Running the command **cd (change directory)** sans arguments will take you back to your home directory
- *cd* is usually run with a single command line argument refering to the location _(path)_ you would like to change to  
```  
    user@bash: pwd  
    /home/ryan  
    user@bash: cd Documents  
    user@bash: ls
    file1.txt file2.txt file3.txt  
```
- When typing a path if you press the tab key it will invoke an auto complete action. This is called a __tab completion__
    - if nothing happens that means there are several possibilities
    - press tab again and it will show you the possibilities
    - continue typing and hit tab once more and it will attempt to auto complete for you

    