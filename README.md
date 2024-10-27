# tutorial1
Basic Git Commands

Here’s a step-by-step hands-on Git tutorial to help you get familiar with Git commands and basic workflows. Follow along by executing these commands in your terminal.

### 1. **Setup Git**

Start by configuring Git with your user information:

```bash
git config --global user.name "Hamza Nadeem"
git config --global user.email "hamzastorm8@gmail.com"
```

This sets your name and email, which will appear in your commit history.

### 2. **Initialize a Git Repository**

Create a new folder for your project:

```bash
mkdir my_project
cd my_project
```

Then, initialize a Git repository:

```bash
git init  # This command will create by default the master branch.

git branch -m "New parent branch name"  # If you want to rename the master branch, use this command"
```

This creates a `.git` directory where Git will store version history.

### 3. **Check the Status of Your Repo**

Check the status of your repository to see if any changes have been made:

```bash
git status
```

Since there are no files, you’ll see something like "nothing to commit, working tree clean."

### 4. **Create Your First File**

Let’s create a simple file:

```bash
echo "Hello Git" > hello.txt
```

Now, check the status again:

```bash
git status  # Using this command again will help us check untracked files and the branch that you are currently on.
```

You’ll see `hello.txt` listed as an untracked file.

### 5. **Add Files to the Staging Area**

To start tracking the file, you need to add it to the staging area:

```bash
git add hello.txt  # This will track and put the file in staging.

git rm --cached hello.txt  # This will untrack or remove the file from staging.
```

Now, check the status again:

```bash
git status
```

The file should be in the "staged" section, ready to be committed.

### 6. **Commit Your Changes**

Commit the file with a message describing what you’ve done:

```bash
git commit -m "Add hello.txt"
```

This saves a snapshot of your changes.

### 7. **Check the Commit History**

You can now see your commit history:

```bash
git log  # This shows the history of committed changes.
```

This shows the commit hash, author, date, and commit message.

### 8. **Modify a File and Commit the Changes**

Make a change to the `hello.txt` file:

```bash
echo "Git is awesome!" >> hello.txt
```

Check the status again to see the changes:

```bash
git status
```

Add and commit the changes:

```bash
git add hello.txt
git commit -m "Update hello.txt with an awesome message"
```

### 9. **Check Differences Between Commits**

You can check the differences between commits using `git diff`. Before staging the changes, run:

```bash
git diff
```

If no changes are detected, try modifying the file again and rerun the command.

### 10. **Create a Branch**

Branches allow you to work on different features without affecting the main codebase:

```bash
git branch feature-branch
```

Switch to the new branch:

```bash
git checkout feature-branch
```

You can now work on this branch independently.

### 11. **Merge a Branch**

After making changes in the `feature-branch`, you can merge it back into the `main` branch.

First, switch back to `main`:

```bash
git checkout main
```

Then merge the changes from `feature-branch`:

```bash
git merge feature-branch
```

### 12. **Push to a Remote Repository**

You’ll need a GitHub, GitLab, or other Git hosting service account. Assuming your repository is hosted on GitHub, first, link your local repository to the remote repository:

```bash
git remote add origin https://github.com/username/my_project.git
```

Then push your local commits to the remote repository:

```bash
git push -u origin main
```

### 13. **Clone a Repository**

To clone an existing repository, use:

```bash
git clone https://github.com/username/another_project.git
```

### 14. **Pull Changes from Remote**

To update your local repository with changes from the remote repository:

```bash
git pull origin main
```

### 15. **Basic Git Workflow Summary**
1. **Modify files** in your working directory.
2. **Stage changes** using `git add`.
3. **Commit changes** with `git commit`.
4. **Push changes** to a remote repository using `git push`.

---

By following these steps, you’ll get comfortable with the basics of Git version control. Let me know if you’d like to dive deeper into any specific Git concepts!
