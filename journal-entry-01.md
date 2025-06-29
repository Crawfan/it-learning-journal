#Journal Entry 01 - Git and SSH Setup

**Date:** 2025-06-28
**Focus Area:** Git, SSH, Remote Repositories 


---

**What I Did:**

- Created a new local Git repository using `git init`.
- Made a directory called `it-learning-journal` and added a `README.md`.
- learned and practiced the Git workflow: `add` --> `commit` --> `push`.
- Used `ssh-keygen` to generate SSH keys for secure GitHub access.
- Added my public SSH key to Github to avoid using username/password.
- Successfully pushed my local commits to GitHub using SSH.


---

**What I Learned:**

- How Git moves files from working directory --> staging --> repository.
- The Purpose of SSH Keys and how they help authenticate Git pushes.
- The difference between local Git (via CLI) and remote Github hosting.
- How to use `echo` and redirection to create files quickly from CLI.

---

**Commands Practiced:**

```bash 
mkdir it-learning-journal
cd it-learning-journal
git init
echo "# Andre's IT Learning Journal" > README.md
git add README.md
git commit -m "Initial commit"
ssh-keygen
git remote add origin git@github.com:crawfan/it-learning-journal.git
git push -u origin master
```

---

**Reflection**

Today I built and linked my first GitHub repository via SSH using only terminal. It was empowering when git accepted my SSH key and i pushed my first commit. 
I now better understand how local and remote Git interact, and this will definitely help in DevOps or sysadmin roles.


---

### Afternoon Update - Hands-on Ansible Practice 


After this morning's GitHub SSH setup, I started working on my Ansible Udemy course by KodeKloud. 

I practiced:

- Writing in YAML
	- Key value pair, Array/lists and Dictionary/Map
- I also went over inventory files and how to set the parameters 
	- talked about using `ini` for smaller networks and `yaml` for larger networks
- Practiced both in the lab environment on KodeKloud

---

**Reflection**

This was great reinforcement of system automation fundamentals, and im starting to see how Ansible is valuable in real-world infrastructure management.
YAML is also becoming more intuitive the more I use it.

---
