## 1. Cloning the ADO Wiki Repository

To start working on the ADO wiki, you need to clone the wiki repository to your local machine. This allows you to create and edit documentation locally.

1. In Azure DevOps, navigate to your project's **Wiki**.
2. Click the **Clone Wiki** button (usually found in the **Wiki** section).
3. Copy the repository URL.

4. In your terminal, clone the repository:
   ```bash
   git clone <URL-OF-THE-WIKI>
   ```
   Replace `<URL-OF-THE-WIKI>` with the actual URL copied from ADO.

---

## 2. Creating a New Branch and Uploading Changes

After cloning the repository, follow these steps to create a new branch, make changes, and push them to the remote repository.

### Step 1: Create a New Branch

To create a new branch where you'll make your changes, use the following command:
```bash
git checkout -b "NameOfBranch"
```
- Replace `NameOfBranch` with a descriptive name for your branch (e.g., `AddingTextControl`).

### Step 2: Make Your Changes

1. Edit or add new documentation files as needed.
2. Use the following commands to stage, commit, and push your changes.

### Step 3: Stage and Commit Changes

To stage all changes for commit, run:
```bash
git add .
```

Then, commit the changes with a message describing what was added:
```bash
git commit -m "Comment about the changes that you added"
```

### Step 4: Push the Branch to the Remote Repository

Push your changes to the remote repository and set the upstream for your branch:
```bash
git push --set-upstream origin NameOfBranch
```
- Replace `NameOfBranch` with the name of your branch.

At this point, your new branch with the changes has been pushed to ADO. You can create a Pull Request (PR) if needed or move to the next step to merge changes into the `wikiMaster` branch.

---

## 3. Merging Your Branch into `wikiMaster` (Main Branch)

In your ADO setup, the main branch is named `wikiMaster`. To merge your changes from your branch into `wikiMaster`, follow these steps:

### Step 1: Fetch the Latest Changes

First, fetch the latest changes from the remote repository to ensure your local repository is up-to-date:
```bash
git fetch origin
```

### Step 2: Checkout the `wikiMaster` Branch

Switch to the `wikiMaster` branch to prepare for merging:
```bash
git checkout wikiMaster
```

### Step 3: Merge Your Branch into `wikiMaster`

Now, merge your changes from your branch into `wikiMaster`:
```bash
git merge origin/NameOfBranch
```
- Replace `NameOfBranch` with your branch's name.

### Step 4: Push the Updated `wikiMaster` Branch

Finally, push the updated `wikiMaster` branch to the remote repository:
```bash
git push origin wikiMaster
```

---

## 4. Handling Merge Conflicts (If Needed)

If there are any conflicts during the merge, Git will notify you. To resolve conflicts, follow these steps:

### Step 1: Resolve Conflicts Manually

Open the conflicting files, manually resolve the conflicts, and save your changes.

### Step 2: Stage and Commit the Resolved Files

After resolving the conflicts, stage the changes:
```bash
git add .
```

Then, commit the merge:
```bash
git commit
```

Now you can continue with pushing the `wikiMaster` branch as outlined earlier.

---
