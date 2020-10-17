# Linux Resources

### Random

- #### Pushing output to a file

  ```bash
  $ ./start.sh > out.txt
  ```

  This will push all console outputs to the out.txt file

- #### Creating Files

  Use `cat` to create files with content in them

  Use `touch` to create files without content in them

  ```bash
  $ touch file1 file2 file3
  ```

- #### Setting up a local server

  ```bash
  $ python3 -m http.server
  ```

  Runs on port 8000. Access files by going to `localhost:8000` in the browser.

  

  If port 8000 is busy for some reason, use any port by:

  ```bash
  $ python3 -m http.server 7800
  ```

  7800 can be replaced with any port number. Access at `localhost:7800` in the browser.

  *https://developer.mozilla.org/en-US/docs/Learn/Common_questions/set_up_a_local_testing_server*

- #### Restart Bluetooth service

  ```bash
  $ sudo service bluetooth restart
  ```

- #### Bose QC35 and Linux!

  Go to [this](https://pandasauce.org/post/bluetooth-on-linux/) link.

- #### Change Unity "Dash Search" size

  ```bash
  $ gsettings set com.canonical.Unity form-factor "Notebook"
  ```

- #### SSH into remote Jupyter-Notebook instance

  First, setup an SSH *Tunnel* to your remote machine

  ```bash
  $ ssh -L 8080:localhost:8080 <remote_user>@<remote_host>
  ```

  This command opens op a new SSH session in the terminal. 

  I've added the -L option that tells SSH to open up a tunnel from port 8080 on the remote machine to port 8080 in my local machine.

  Next, launch Jupyter without the browser, on a specific port (8080 in this case)

  ```bash
  $ jupyter notebook --no-browser --port=8080
  ```

  Finally, click the link that is shown, and enjoy!

  *Ref:* *https://fizzylogic.nl/2017/11/06/edit-jupyter-notebooks-over-ssh/* 
  
- #### Creating Symbolic Links

  Creates a symlink of `~/Applications/MATLAB`  at `/usr/local/` so that Linux thinks that `MATLAB` is in `usr/local`

  ```bash
  $ sudo ln -s ~/Applications/MATLAB /usr/local/
  ```

  *Ref: https://www.freecodecamp.org/news/symlink-tutorial-in-linux-how-to-create-and-remove-a-symbolic-link/*
  
- #### Creating Aliases

  Aliases are like shortcut commands in a shell

  1. edit the `.bashrc` file

     ```bash
     $ vim ~/.bashrc
     ```

     ```bash
     # custom aliases
     alias jpn='jupyter-notebook'
     ```

  2. Update the aliases by sourcing the `.bashrc`

     ```bash
     $ source ~/.bashrc
     ```

  Now to run `jupyter-notebook` just type `jpn` !

### Visual Studio

+ #### Opening as a super user

  ```bash
  $ sudo code /path/to/folder/or/file --user-data-dir
  ```

+ #### Auto updating

  ```bash
  $ wget https://vscode-update.azurewebsites.net/latest/linux-deb-x64/stable -O /tmp/code_latest_amd64.deb
  $ sudo dpkg -i /tmp/code_latest_amd64.deb
  ```

  Comment - make into a bash script at some point

### Bash Scripting

+ [Beginner/Bash scripting][https://help.ubuntu.com/community/Beginners/BashScripting?highlight=%28Beginners%2F%29]

+ [Another Guide][https://www.tldp.org/LDP/abs/html/part1.html]

+ #### Saving your BASH scripts

  First give executable access to the bash script file

  ```bash
  $ chmod a+x yourBashScript
  ```

  Then, if it's your first time, you need to create a Custom Bash Scripts folder and then add that to the `$PATH` variable. 

  Remember to save your bash script **without** an extension

  ```bash
  # if you don't want to create a custom bash scripts folder, then add your bash script to /usr/local/bin because that is already part of the `$PATH` variable
  
  $ mv yourBashScript /usr/local/bin
  ```

  ```bash
  # otherwise
  
  $ cd /usr/local/bin
  $ mkdir custom-bash-scripts
  ```
  
  Add the folder to the `$PATH`
  
```bash
  # open ~/.bashrc
$ sudo gedit ~/.bashrc
  
  # add the next line to the end of the file
  
# exports the `$PATH` variable to include our new folder
  export PATH="$PATH:/usr/local/bin/custom-bash-scripts"
```

  

  Then move your file to the new folder

  ```bash
  $ mv yourBashScript /usr/local/bin/custom-bash-scripts
  ```

  Run your script from anywhere by typing the script name:

  ```bash
  $ yourBashScript
  ```

### Why Vim?

- [Why I Still Use Vim][https://medium.com/commitlog/why-i-still-use-vim-67afd76b4db6]
- http://vimcasts.org/
- [Practical Vim book][https://www.amazon.com/Practical-Vim-Edit-Speed-Thought/dp/1680501275/ref=as_li_ss_tl?ie=UTF8&qid=1501817867&sr=8-3&keywords=vim&linkCode=sl1&tag=caspbeye-20&linkId=6c394064b4e6f05b198e68c64a6f4d76]
- [Vim as my LaTeX editor][https://medium.com/rahasak/vim-as-my-latex-editor-f0c5d60c66fa]

### Git

1. Initialising a new project as a git repo
   - https://kbroman.org/github_tutorial/pages/init.html
2. Book on git stuff
   - https://happygitwithr.com/

## Blogs

1. https://shapeshed.com/
2. 

[https://help.ubuntu.com/community/Beginners/BashScripting?highlight=%28Beginners%2F%29]: