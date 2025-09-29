# Week 4 — Practicing Git & GitHub

## 📖 Objectives
By the end of this week’s class, you should be able to:
- Fork and clone the course repository to your computer.
- Navigate into the correct folder before cloning.
- Understand the difference between **forking** (copy on GitHub) and **cloning** (copy on your computer).
- Create and switch to a new branch.
- Add, commit, and push changes to your fork.
- Authenticate with GitHub using a **Personal Access Token (PAT)** when pushing over HTTPS.

---

## 🛠️ Step 1 — Fork the instructor repo
1. Go to the instructor repo:  
   👉 [https://github.com/MonirehRazavi/literature-in-motion](https://github.com/MonirehRazavi/literature-in-motion)  
2. Click **Fork** (top-right).  
3. You now have your own copy, for example:  
   👉 `https://github.com/AnneSmith/literature-in-motion`

---

## 🛠️ Step 2 — Navigate to your class folder
Before cloning, make sure you are inside the folder where you want to keep this project.

```bash
cd ~/Documents/LiteratureInMotion     # go into your course folder
pwd                                   # check where you are
ls                                    # list contents of the folder

---


## 🛠️ Step 3 — Clone your fork

Use your fork’s URL (replace <your-username> with your GitHub username).

```bash
git clone https://github.com/<your-username>/literature-in-motion.git
cd literature-in-motion

Check you cloned your fork (not the instructor’s):

```bash
git remote -v


Expected:

```bash
origin  https://github.com/<your-username>/literature-in-motion.git (fetch)
origin  https://github.com/<your-username>/literature-in-motion.git (push)
