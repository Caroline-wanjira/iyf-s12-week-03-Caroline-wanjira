# Terminal Log - Task 5.1

Commands I ran in Git Bash, in order, and what each did.

## Exercise 1: Basic Navigation

- `mkdir ~/terminal-practice && cd ~/terminal-practice` - failed with "File exists" because the folder was already there
- `cd ~terminal-practice` - typo (missing `/`), gave "No such file or directory"
- `cd ~/terminal-practice` - moved into the practice folder
- `pwd` - printed /c/Users/Alex/terminal-practice
- `ls` - printed nothing, the folder was empty
- `cd ~/Documents` - moved into my Documents folder
- `pwd` - printed /c/Users/Alex/Documents
- `cd ~` - went to my home directory
- `pwd` - printed /c/Users/Alex
- `cd ~/Documents` then `cd ..` - went into Documents, then back up one level
- `pwd` - printed /c/Users/Alex

## Exercise 2: Create Project Structure

- `cd ~/terminal-practice` - moved back into the practice folder
- `mkdir -p my project/src/css my-project/src/js my project/src/images` - typo (spaces instead of hyphens), created stray folders `my` and `project`
- `mkdir my-project/docs my project/tests` - typo, gave "File exists" error
- `ls` - showed `my/`, `my-project/` and `project/`
- `rm -r my project` - removed the two stray folders
- `mkdir -p my-project/src/css my-project/src/js my-project/src/images` - created the nested src folders
- `mkdir -p my-project/docs my-project/tests` - created docs and tests folders
- `touch my-project/README.md` - created an empty README file
- `ls -R my-project` - listed the whole structure to check it matched the task