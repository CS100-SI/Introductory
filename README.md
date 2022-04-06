# Getting Familiar with GitHub
We will be using GitHub for the majority of this quarter. This includes any practice problem code or study guides, etc.
To start off, get yourself familiar with all these terminal commands and Git commands.

### Terminal Commands
* `pwd` - Print Working Directory: displays currently directory
* `ls` - List: lists directories and files in current director
  * Appending `-l` displays directories and files w/ permissions & last edit time
  * Appending `-a` displays all directories and files **including hidden files**
  * Appending `-la` or `al` combines the power of `-l` and `-a`
  * Appending a folder name (i.e. `ls home/` lists files in that directory without entering it)
* `cd` - Change Directory: changes working directory
  * `cd ..` exits current directory and enters previous direct
    * If you are in `home/homework`, typing `cd ..` will take you to `home/`
  * `cd` by itself or `cd ~` changes working directory to ROOT directory
  * Appending a directory path will take you directly to that directory
    * ex) `cd home/homework/CS10B` takes you to the CS10B folder in homework, which is in home
    * `..` can be used as well
      * ex) If you're in `home/homework/CS100`, typing `cd ../../labs` will take you to the labs folder in `home`
* `mkdir` Creates a directory given a name
* `touch` Creates a file given a name (must include file type in name)
* `cp` Copies a file into a specified directory
  * ex) `cp main.cpp ../homework/CS100`
* `rm` Removes a FILE
  * appending `-rf` will remove a FOLDER and all contents within (You don't get a confirmation message)
* `mv` Moves a file into a specified directory
  * ex) `mv main.cpp ../homework/CS100`
  * Specifying another file name will *rename* the file
    * ex) `mv main.cpp run.cpp`
* `cat` Displays all contents within the specified file onto the terminal
* `nano` or `vim` Opens the specified file in an in-terminal file editor
  * Note: Nano is more simple than vim; vim focuses on keeping your hands on the home-row, which means your arrow movements use the homerow
* `g++ -Wall -Werror main.cpp -o run.out` Compiles a C++ code
  * `-Wall` tells compiler to display all warnings into the terminal
  * `-Werror` tells compiler to treat all warnings as errors
  * `-o` tells compiler to create executable using following argument
    * `-o run.out` creates a `run.out` executable rather than the default `a.out`
  
### Git Commands
Main commands:
* `git init` initializes a **new** repository for the directory you're in
* `git clone [url]` clones an **existing** repository onto your local machine
* `git status` shows what files have been changed and what have been added to the staging phase
  * Use this once before you use `git add` to see what files need to be added
* `git add [filename]` adds a file or entire directory into the staging phase
  * Use `git add *` to add **all** un-staged changes
* `git reset [filename]` removes a file or entire directory from the staging phase
* `git commit` commits your staged files
  * This will open a file, where you can provide a message and description
  * Use `git commit -m "[message]"` to do a quick commit message without opening a file
    * Use this if your message is **less than 15 words**, otherwise use the normal commit
* `git branch` lists all branches available
* `git branch [name]` creates a new branch
  * `git push -u origin [name]` pushes the new branch onto the repo
* `git merge [branch]` merges the specified branch into the one you're currently in
* `git fetch` fetches any changes to repo, including branches
* `git push` pushes any committed changes
  * Multiple commits can be stacked before a push
* `git reset --hard [commit]` completely clears the staging phase and the commits
  * Usually, you'll be using `git reset --hard HEAD`
* `git stash` saves any staged and modified changes.
  * Usually you'll do this if you made changes, but need to visit another branch
  
## Practice
* Clone the repo
  * https://github.com/CS100-SI/Introductory
* Create a new branch and enter it
  * Name the branch with your first name and last name initial
    * i.e. JohnT
* Create a `main.cpp` in your branch and commit it
  * Have it print your favorite hobby/pastime
* Push the branch on to the repo
* Open a pull request in GitHub using the `Pull requests` tab and `New pull request`.
  * You have successfully done this practice if I **reject** the request without labeling an `Issue` to it.

For all repos in these sessions, you will be essentially repeating the above steps