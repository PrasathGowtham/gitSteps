# gitSteps
Steps about git pull push
This works for any Git repository — local or remote (GitHub, GitLab, Bitbucket, etc.).

🧠 Step-by-Step Git CLI Commands
1️⃣ Check your current branch
git status


→ This shows if you have any uncommitted changes and what branch you’re on.
If you’re not sure which branch:

git branch

2️⃣ Stash or commit your local changes

If you have uncommitted changes and want to keep them:

git add .
git commit -m "Your commit message"


If you’re not ready to commit yet:

git stash


(You can reapply later using git stash pop)

3️⃣ Pull the latest code from remote

If you’re on a feature branch:

git pull origin your-branch-name


If you’re on main or master:

git pull origin main


⚠️ This merges remote changes into your local branch.

4️⃣ Fix any merge conflicts (if any)

If you see conflicts:

Open the conflicting files (marked with <<<<<<< and >>>>>>>)

Resolve manually
Then run:

git add .
git commit -m "Resolve merge conflicts"

5️⃣ Merge another branch (optional)

If you want to merge another branch into yours:

git merge branch-to-merge


Example:

git merge main

6️⃣ Push your merged code to remote

Once merged and tested:

git push origin your-branch-name


or for main:

git push origin main

🧰 Optional (for a cleaner workflow)
Rebase instead of merge (for a linear history)
git pull --rebase origin main

Push after rebase
git push origin your-branch-name --force-with-lease


⚠️ Only use --force-with-lease if you’re sure others haven’t pushed to the same branch — it rewrites commit history safely.

✅ Full Command Summary (Cheat Sheet)
# 1. Check your branch
git status
git branch

# 2. Save or commit your work
git add .
git commit -m "Your changes"

# 3. Pull the latest code
git pull origin main     # or your branch

# 4. Resolve any conflicts
# (edit → add → commit)

# 5. Push your changes
git push origin main     # or your branch
