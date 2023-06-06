# Git Commands
A list of Git commands I frequently used.

---

### Example of uploading a local repository to remote server.
  1. Initialize a local repository: 
      ```bash
      git init
      ```
  2.  Change the branch name to match the branch name on GitHub or error will occur
      ```bash
      git branch -m master main
      ``` 
  3.  Staged files
      ```bash
      git add .
      ``` 
      - Staging specific files
        ```bash
        git add <file1> <file 2> <file 3>
        ``` 
      - Unstaging specific files
        ```bash
        git reset <file1> <file 2> <file 3>
        ``` 
      - Unstaging all files
        ```bash
        git reset
        ``` 
  4.  Check does files staged correctly
      ```bash
      git status
      ``` 
  5.  Commit Files
      ```bash
      git commit -m "<your message here>"
      ``` 
  6.  Check if in the right branch
      ```bash
      git branch
      ``` 
  7.  Connect to remote server (origin = remote name)
      ```bash
      git remote add origin <GitHub repository url>
      ```     
  8.  Check if connect to the correct remote server
      ```bash
      git remote -v
      ```  
  9.  Always pull before push (origin = remote name, main = local branch)
      ```bash
      git pull origin main
      ``` 
      - If the files on remote are incosistent with local repository (Example: there is a README.md on remote server that local repository does not have)
        ```bash
        git pull origin main --allow-unrelated-histories
        ``` 
  10. Push to remote server (origin = remote name, main = local branch)
      ```bash
      git push origin main
      ``` 
---
### Other useful commands
  - Clone a repository from remote server
    ```bash
     git clone <GitHub repository url>
    ``` 
  - Create new branch
    ```bash
     git branch <Branch name>
    ``` 
  - Switch new branch
    ```bash
     git checkout <Branch name>
    ``` 
  - Review commit histories
    ```bash
     git log
    ``` 
    - Review n commit histories
      ```bash
       git log -n <count>
      ``` 
  - Review file differences between local directory and staged area
    ```bash
     git diff <File name>
    ``` 
  - Review file differences between staged area and remote server
    ```bash
     git diff --staged <File name>
    ``` 
  - Ignore certain files/directories in local repository to be push to remote repository
    1. create a .gitignore in local repository directory and open it
    ```bash
     touch .gitignore
    ``` 
    ```bash
     vi .gitignore
    ``` 
    2. add files/directories to be ignored, and save it (esc -> :wq) 
       - ![Image](/Images/gitIgnoreTutorial.png)
    3. finally push .gitignore to remote repository  

  - Undo an accidental deleted files/directories after git pull request
    1.  Use git reflog to track all changes
    ```bash
     git reflog
    ``` 
    2.  switch to the desired Head index ( n = desired index)
    ```bash
     git checkout HEAD@{n}
    ``` 
