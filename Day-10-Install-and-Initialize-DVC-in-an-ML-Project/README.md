# ❤️ Day 10 - Install and Initialize DVC in an ML Project
---

### Step 1: Navigate to the Repository

First, open your terminal and change your working directory to the root of your project where the Git repository is located.

```bash
cd /root/code/fraud-detection/

```

### Step 2: Initialize DVC

Run the initialization command. This sets up the internal DVC configuration files and tracking structures without altering your existing Git history.

```bash
dvc init

```

*What this does:* This creates a `.dvc/` directory (which contains configurations, cache settings, and state files) and a `.dvcignore` file in your project root.

### Step 3: Verify the Changes (Optional but Recommended)

To see the new files that DVC created and how Git perceives them, run:

```bash
git status

```

You should see `.dvc/` and `.dvcignore` listed under untracked files, while `.dvc/cache` and other local-only files are automatically ignored via an internal `.gitignore` created by DVC.

### Step 4: Stage the DVC Files in Git

Stage all the newly created DVC configuration files so they are ready to be tracked by Git.

```bash
git add .dvc .dvcignore

```

### Step 5: Commit the Initialization to Git

Record the initialization by creating a new Git commit with the exact required message.

```bash
git commit -m "Initialize DVC"

```


