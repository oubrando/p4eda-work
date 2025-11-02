# HW3A Solution - Git and Version Control
## Part 1: Repository Cloning
I successfully cloned the class repository from `https://github.com/olearydj/INSY6500` to
`~/insy6500/class_repo`.
### Key Commands Used
- `git clone <url>` - Create local copy of remote repository
- `git log` - View commit history
- `git remote -v` - Check remote repository connections
## Part 2: Portfolio Repository Creation
I created my personal course repository with:
- Professional README.md describing the project
- Proper .gitignore to exclude unnecessary files
- Organized directory structure for homework, projects, and notes
### Understanding Git Workflow
The three-stage workflow:
1. Working Directory: Where I edit files
2. Staging Area: Where I prepare commits with `git add`
3. Repository: Where commits are permanently stored with `git commit`

## Part 3: GitHub Publishing
Successfully published repository to GitHub:
- Used `git remote add origin` to connect local repo to GitHub
- Used `git push -u origin main` to upload commits
- Verified all files and commits are visible on GitHub
### The Remote Connection
My local repository is now connected to GitHub:
- `git remote -v` shows the remote URL
- `git push` will send my commits to GitHub
- `git pull` will get updates from GitHub (if changes are made on GitHub)
### Details
Complete this section with details from your setup:
- Repository URL: `https://github.com/oubrando/p4eda-work`
- Output of `git remote -v`:
    - `origin  https://github.com/oubrando/p4eda-work.git (fetch)`
    - `origin  https://github.com/oubrando/p4eda-work.git (push)`
- The output of `git log --oneline`:
    - 45b5c64 (HEAD -> main, origin/main) Complete Part 3 documentation
    - 7904d19 Add hw3a solution document
    - cd05a0b Initial commit: Add README and .gitignore

## Questions

### Reflections

#### Question 1 
a) I've used Git professionally for several years.  Prior to that, I managed file versions primarily through the file names ("_final_brandon_version_23_Sep_2010").  This got pretty messy, especially when there were many version changes and authors. Git provides many advantages:
1. Author traceability:  Git makes it easy to retain who did what to a file.  This is especially true when used within an IDE extension like Git Lense.
2. Branching:  Making changes in a separate branch allows for testing and peer reviews to happen without introducing errors to the main product
3. History: It's easy to go back to previous versions in the event of mistakes.

b) Git's commit history would have been valuable in collaborative projects where multiple people contributed to the final document.  I've seen several occasions where document versions diverged and had to be reconciled at the end.  Having Git's commit history as the authoritative document would have helped greatly. Of course, this approach would only be effective if the team members maintained committing best practices. 

#### Question 2: Repository Organization

a) Keeping repos separate prevents accidental overrwriting of class files and merge conflicts between students

b) I will be good practice to have a personal repo for individual assignments, individual repos for different group assignments, and a references repo.  This will allow appropriate separation of permissions and file hygiene. 

#### Question 4:  Commit Messages and History

a) The second commit message is more useful because it clearly states what changes are made to the repo without having to look at the diff.  You might need this commit if you need to cherry pick the changes to another branch or tracing its author. 

b) Commits should be made frequently to prevent divergence between team members. A unit of work should achieve a singular and complete (the code is runnable) change. 

### Graduate Questions

#### Question 1 

a) It was valuable to commit the README and .gitignore separately from hw3a-solution.md to allow easier traceability and revertibility in the event of a significant error in the solution file. If all files had been committed at once, it would be less clear who made the changes and why. It also allows progressive saving in the event of a system failure.

b) I would commit the update load-data code (assuming it's complete and running), the typo, and the README update in separate commites.  Staging allows me to have the half-finished work in my local repo without being committed.  It also allows me to deliberately decide which changes go into which commit, even if they all exist together in the repo.

c) `git status` allows you to quickly see what has been changed and what is staged for commit.  You should use it before staging to view the changes that have been made (candidates for commit) and before committing to verify all staged files are desired. It can also be used to verify you are on the expected branch

#### Question 2

a)  "Distributed" in this context means a copy of the repo is stored on your local machine as well as the Github repo.  Google Drive and Dropbox are centralized systems, which means single shared files are modified as edits are made.

b) This decentralized architecture is valuable because it allows you to work separately from others without interference.  This allows developers to work separately and push only desired working changes to the shared repo when they are ready.  Conflicts can arise when separate developers make changes to the same code, but resolving them through Git's tools is a better than the invisible conflicts that are possible when two or more people are modifying a shared file. 

c) `git clone` creates a full copy of the remote repo. It is for initiating a local repo.  `git pull` is used to pull any changes to the remote repo once it is in place locally.  I can pull from the class repo because it is a public repo, but I cannot push because I am not a contributor to the repo.  I can read and write to my own repo because I am an approved contributor.

#### Professional Portfolio

a) I'll remain biased to the smallest, self-contained (working) changes possible.  Occasional mistakes are expected, but the advantages of numerous small changes over large including mistake corrections and refinements is preferential to larger more polished changes. This will also help prevent losing finished work due to computer malfunctions. 

b) A README for a portfolio repo should read more like a cover letter explaining who you are, your objectives, and contact information.  An open-source project's README should introduce the project's objectives, dependencies, and initial instructions.

c) Building this portfolio over time will allow prospective employers to view my activity over time, providing evidence that I follow best practices and that the work is mine.  A habit of clear documentation in commit messages and user instructions will make this a more valuable portfolio for me and others. 