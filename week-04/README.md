# Week 4 —  Git & GitHub

## 📖 Objectives
By the end of this week’s class, you should be able to:
- Fork and clone the course repository to your computer.
- Navigate into the correct folder before cloning.
- Understand the difference between **forking** (copy on GitHub) and **cloning** (copy on your computer).
- Create and switch to a new branch.
- Add, commit, and push changes to your fork.
- Authenticate with GitHub using a **Personal Access Token (PAT)** when pushing over HTTPS.

---

## 🤹 Hands-on: Branches, Folders, Files, and Commits

We will now practice the full cycle:  
- Check which branch you’re on.  
- Create folders and files.  
- Stage changes.  
- Commit changes.  
- Push everything to your fork.  

The commands are the same on **Mac** and **Ubuntu/WSL**.

---

### Step 4 — Check your current branch
First, let’s see which branch you are on.

```bash
git branch
```

- The branch with a `*` is your current branch.  
- If you are still on `main`, create and switch to your personal branch:

```bash
git checkout -b week4-<yourname>
```

👉 This keeps your changes separate and safe.

---

### Step 5 — Make a notes folder and file
We’ll add a **new folder** and a **personal note file**.

```bash
mkdir -p notes
echo "This is my first Week 4 note" > notes/<yourname>.txt
```

**Commit explanation:**  
This commit will record the creation of the `notes/` folder and your first text file inside it. It shows the moment you started adding personal notes for Week 4.

```bash
git add notes/<yourname>.txt
git commit -m "Add my Week 4 note"
```

---

### Step 6 — Make a maps folder and placeholder file
Now let’s add a `maps/` folder. Git ignores empty folders, so we add a small “placeholder” file to keep the folder tracked.

```bash
mkdir -p maps
echo "placeholder for maps" > maps/.keep
```

**Commit explanation:**  
This commit documents that you prepared a `maps/` folder for future mapping projects. Even though it’s empty now, the commit makes sure everyone will have the same structure in their repos.

```bash
git add maps/.keep
git commit -m "Add maps folder with placeholder file"
```

---

### Step 7 — Make a data folder and simple CSV file
Next, create a `data/` folder and add a tiny CSV file with sample content.

```bash
mkdir -p data
echo "name,city" > data/class.csv
echo "Anne,Ottawa" >> data/class.csv
```

**Commit explanation:**  
This commit saves your first structured dataset (`class.csv`) in the `data/` folder. It shows that you practiced creating and storing tabular data in the repo.

```bash
git add data/class.csv
git commit -m "Add class.csv with sample data"
```

---

### Step 8 — Push your branch to GitHub
Now we’ll send all of your commits to GitHub.  
The first time you push, Git will ask for your **GitHub username** and **Personal Access Token (PAT)**. Paste your PAT when it asks for your password.

```bash
git push -u origin week4-<yourname>
```

**Commit explanation:**  
This is not a new commit — it uploads the three commits you already made to your fork on GitHub so you can see them online.

---

### Step 9 — Verify online
1. Go to your fork on GitHub.  
2. Switch to your `week4-<yourname>` branch.  
3. You should now see three commits in your history, corresponding to:  
   - Adding `notes/<yourname>.txt`  
   - Adding `maps/.keep`  
   - Adding `data/class.csv`  

---

## ✅ What you practiced
- Checking and creating branches.  
- Adding new folders and files.  
- Writing clear commit messages.  
- Understanding that each commit is a snapshot of your work.  
- Pushing commits to your fork and verifying them online.
