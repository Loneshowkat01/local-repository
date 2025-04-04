# Configuring Git
To configure Git with your user details, run:
```
git config --global user.name "showkat"
git config --global user.email "loneshowkatsss6@gmail.com"
```
# Basic Git Commands

## 1. Cloning a Repository
Cloning means making a duplicate of a repository from **GitHub (remote)** to **local (PC)**.
```bash
git clone <repository_link>
```
- To get the repository link, go to GitHub, click on **Code**, and copy the HTTPS link.
- Example:
```bash
git clone https://github.com/yourusername/repository.git
```
- The repository is now cloned successfully to your local machine.

---

## 2. Navigating in Terminal
- **Change Directory:**
  ```bash
  cd <folder_name>
  ```
  Example:
  ```bash
  cd first_showkatrepository
  ```
- **List Files:**
  ```bash
  ls
  ```
  This command shows all files in the current directory.

---

## 3. Checking Repository Status
- **Check status of files:**
  ```bash
  git status
  ```
  - If files are the same as in GitHub → *"Up to date"*
  - If local files are different → *"Modified"*
  - If there are new files → *"Untracked"*

## 4. Understanding File States in Git
- **Modified**: File is changed after commit.
- **Untracked**: New file added that Git does not yet recognize.
- **Unmodified**: No changes made.
- **Staged**: File is ready to be committed.

### Example Workflow:
1. Create a new file **index.html** in `first_showkatrepository`.
2. Check status:
   ```bash
   git status
   ```
   It will show "untracked file" because Git doesn’t know about this new file.
3. **Stage the file** (take a screenshot of its state):
   ```bash
   git add index.html
   ```
   Now, the file is ready to be committed.
4. **Stage multiple files at once:**
   ```bash
   git add README.md
   ```
   OR
   ```bash
   git add .
   ```
   (The `.` stages all changes in the repository.)

---

## 5. Committing Changes
- **Commit records a snapshot of the staged changes.**
  ```bash
  git commit -m "Your commit message here"
  ```
- Example:
  ```bash
  git commit -m "Added index.html file"
  ```
- After committing, you may see:
  ```
  Your branch is ahead of 'origin/main' by X commits.
  ```
  This means the local repository has changes that are not yet pushed to GitHub.

---

## 6. Pushing Changes to GitHub
- **Push local commits to GitHub:**
  ```bash
  git push origin main
  ```
- This updates GitHub with the latest local changes.

---

# Creating a Local Repository and Uploading to GitHub

### Opposite of Cloning (Local to Remote)
Instead of cloning from GitHub, we create a local repository first, then push it to GitHub.

### Steps:
1. **Initialize a new Git repository**:
   ```bash
   git init
   ```
   - This converts the local folder into a Git repository.
   - To verify, check for hidden files:
     ```bash
     ls -a
     ```
     If `.git` appears, the folder is now a Git repository.
2. **Create new files (e.g., index.html, style.css)**.
3. **Stage and commit the files:**
   ```bash
   git add .
   git commit -m "Initial commit"
   ```
4. **Connect the local repository to GitHub:**
   ```bash
   git remote add origin <GitHub_Repo_Link>
   ```
   Example:
   ```bash
   git remote add origin https://github.com/yourusername/newrepo.git
   ```
5. **Verify the remote link:**
   ```bash
   git remote -v
   ```
   This checks where Git is pushing changes.
6. **Check and rename the branch (optional):**
   ```bash
   git branch
   git branch -M main
   ```
7. **Push the local repository to GitHub:**
   ```
   git push origin main
   ```



