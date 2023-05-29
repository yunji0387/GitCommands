# Git Commands
## A list of Git commands I frequently used.

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
      - Unstaging specific files
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
  9.  Always pull before push (origin = remote name)
      ```bash
      git pull origin main
      ``` 
  10. Push to remote server (origin = remote name)
      ```bash
      git push origin main
      ``` 
