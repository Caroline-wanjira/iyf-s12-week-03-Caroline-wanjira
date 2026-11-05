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


## Task 5.2: File Operations (practice in ~/terminal-practice/my-project)

- `touch index.html` - created an empty file
- `cat index.html` - printed nothing because the file is empty
- `cp index.html backup.html` - copied the file
- `mv backup.html docs/` - moved the copy into docs
- `rm home.html` - failed ("cannot remove"), because I hadn't renamed index.html yet
- `ls` - showed index.html, so the rename had not happened
- `mv index.html home.html` - renamed the file
- `rm home.html` - deleted the file
- `cp -r src/ src-backup/` - copied the src directory
- `mv src-backup/ archive/` - renamed the copy to archive
- `rmdir archive/` - failed, because the directory was not empty
- `rm -r archive/` - deleted the directory with its contents
- `ls` - confirmed archive was gone


## Task 5.3: Useful Terminal Commands 

- `find . -name "*.html" | wc -1` - typo (number 1 instead of letter l), gave "unknown option -- 1"
- `find .-name "*.html" | wc -l` - typo (no space after the dot), gave "No such file or directory"
- `find . -name "*.html" | wc -l` - printed 4, so there are 4 HTML files
- `grep -rl "contact" --include="*.html" --include="*.css" .` - listed about.html, contact.html, index.html, projects.html and styles.css as containing "contact"
- `wc -l styles.css` - printed 380, so the CSS file has 380 lines
- `history | tail -10` - showed my last 10 commands (entries 5 to 14)

## Task 5.4: Shell Script Basics

- Created `new-project.sh` in the week-03 repo with the project setup script
- `chmod +x new-project.sh` - made the script executable
- `cd ~/terminal-practice` - moved to the scratch folder, outside the repo
- `bash ~/Desktop/iyf-s12-week-03-Caroline-wanjira/new-project.sh sunrise-notes` - created the project structure
- `ls -R sunrise-notes` - showed README.md, docs, tests and src (css, js, images, index.html)
- `bash ~/Desktop/iyf-s12-week-03-Caroline-wanjira/new-project.sh` - no name given, printed the Usage message

## Task 6.1
- Verified Git configuration
- Practised git init
- Created three commits

## Task 6.2
* Practised creating and switching branches using `git branch` and `git checkout` / `git switch`
* Created `feature/about-page` branch, updated `about.html`, merged into `main`, and deleted the feature branch
* Created two conflicting branches (`feature/header-one` and `feature/header-two`) to simulate a merge conflict
* Resolved the merge conflict manually in `about.html` by editing conflict markers and committing the result

## Stimulated collaborator update