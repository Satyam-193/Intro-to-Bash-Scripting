# Intro-to-Bash-Scripting

Bash scripting is a way to automate tasks on Linux and macOS systems. It involves writing a series of commands in a plain text file, which is then executed by the Bash shell.
<br/><br/>

- pwd: Print Working Directory.
  ```
  ~$ pwd
  /home/ubuntu
  ```
- whoami: print the current username of loggedin user.
  ```
  ~$ whoami
  ubuntu
  ```
- man: display thecomplete manual of the asked command in pages .
  ```
  ~$ man [option] [command]
   ~$ man ls
  ```
- help: display the brief information of the command.
  ```
  ~$ ls --help
  ```

File Manipulation:

- cd: Change directory to certain location by providing path from the start of root directory ('/') or current directory ('.').
  ```
  ~$ cd path
  ```
  Change the path to home Directory.
  ```
  ~$ cd /home
  ```
  " . " represent current directory so pwd i.e. (print working directory or current working directory path) will not change
  ```
  ~$ cd .
  ```
  change to parent directory
  ```
  ~$ cd ..
  ```
  change to home directory
  ```
  ~$ cd ~
  ```
  change to two level up of current directory (if pwd is /home/ubuntu then after this command pwd become root ('/') directory.
  ```
  ~$ cd ../..
  ```
- ls: List the contents of a directory.
  <br/>
  ```
  ~$ ls
  ```
  List the hidden content in the Directory.
  ```
  ~$ ls -a
  ```
  List the given permission (using ls -l) and hidden content (ls -a) in the Directory.
  ```
  ~$ ls -la
  ```
  List the content of the Directory using the path.
  ```
  ~$ ls /path
  ```
  <br />
- mkdir: Create a new directory. Using -p you can create subdirectories.
  ```
  ~$ mkdir folder_name1  -p folder_name1/folder_name2
  ```
- touch: Create an empty file.
  ```
  ~$ touch myfile.txt
  ```
  Create Multiple files using single command
  ```
  ~$ touch file{1..5}.txt
  file1.txt file2.txt file3.txt file4.txt file5.txt
  ```
- cp: Copy a file or directory. This command creates a copy of the `source_file` at the specified `destination_path`
  ```
  ~$ cp source_file destination_path
  ```
  Copy multiple files to a `destination_path`
  ```
  ~$ cp a.txt b.txt c.txt new/
  ```
  
- mv: Move or rename a file or directory. (e.g. mv file1.txt renamed_file.txt renames file1.txt)
  ```
  ~$ mv source_file destination_path
  ```
- rm: Remove a file or directory (use with caution!). (e.g. rm file1.txt removes file1.txt)
  ```
  `$ rm file.txt
  ```
  Remove the Non Empty Directory Recursively.
  ```
  `$ rm -r folder
  ```
  Remove the Non Empty Directory Recursively and forecfully.
  ```
  `$ rm -rf folder
  ```
  
<br/>
<br/>
Text and Output:

- echo: Print text to the terminal. (e.g. echo Hello World! prints "Hello World!")
  ```
  ~$ echo "Hello World"
  Hello World
  ~$ echo target.com
  ```
  Store the content in a file
  ```
  ~$ echo "Hello World" > hello.txt
  ~ $ cat hello.txt
  Hello World
  ```
  Overwrite the content of a file
  ```
  ~$ echo "World" > hello.txt
  ~ $ cat hello.txt
  World
  ```
  Append the content of a file
  ```
  ~$ echo ", Good to see you" >> hello.txt
  ~ $ cat hello.txt
  Hello World, Good to see you
  ```
  
- cat: Display the contents of a file, also can overwrite and append the content in same way as the echo command. 
  ```
  ~$ cat message.txt
  ```
  
- grep: Search for a pattern within a file. (e.g. grep error log.txt searches for "error" in log.txt)
  ```
  ~$ cat log.txt | grep "error"
  ```
<br/>
<br/>
Basic Scripting Elements:

- #: Used for comments (ignored by the shell).
- $: Used to access variables. (e.g. name="John" sets a variable named "name")
<br/>
<br/>
