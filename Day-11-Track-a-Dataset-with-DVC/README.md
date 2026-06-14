# ❤️ Day 11 - Track a Dataset with DVC
---

### 🧑‍💻 1: Open the Project Directory

Ensure you are in the root of your project repository where DVC and Git are initialized.

```bash
cd /root/code/fraud-detection/

```

### 🧑‍💻 2: Stop Git Tracking the Dataset (Without Deleting It)

To remove the file from Git's index while keeping it intact on your local disk, use the `git rm --cached` command.

```bash
git rm --cached data/raw/transactions.csv

```

### 🧑‍💻 3: Track the Dataset with DVC

Now, hand over the tracking responsibility to DVC. This command will create a `transactions.csv.dvc` pointer file and automatically append the dataset's path to `data/raw/.gitignore` so Git ignores the actual raw data file in the future.

```bash
dvc add data/raw/transactions.csv

```

### 🧑‍💻 4: Stage the Changes for Git

You now need to tell Git to track the newly created `.dvc` pointer file and the updated `.gitignore` file.

```bash
git add data/raw/transactions.csv.dvc data/raw/.gitignore

```

### 🧑‍💻 5: Commit the Changes to Git

Finally, record the transition in your Git history with the requested commit message.

```bash
git commit -m "Track transactions dataset with DVC"

```

---

### Verify the Setup

To ensure everything was executed perfectly, you can verify using two methods:

1. **Terminal Check:** Run `git status`. You should see that `data/raw/transactions.csv` is no longer tracked or listed as an untracked file, while the `.dvc` file is safely committed.
2. **VS Code Explorer:** Look at the **EXPLORER** panel on the left. Under the **DVC TRACKED** section, `transactions.csv` should now be visible, confirming that the DVC extension successfully recognizes it as a managed asset.
