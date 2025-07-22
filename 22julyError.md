git push -u origin main

ERROR: Permission to Shubhanjali01/INTERVIEWS.git denied to Reah99.
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.


**Solution**
This means that Git is trying to push the code using the wrong GitHub user (Reah99) instead of Shubhanjali01 — the actual owner of the repo.


- Option 1: If You Own the Repository (on GitHub account Shubhanjali01)

✅ Step 1: Check your current Git config
command- 

git config user.name
git config user.email


✅ Step 2: Set correct GitHub remote URL (HTTPS method)
git remote set-url origin https://github.com/Shubhanjali01/INTERVIEWS.git

then try 
git push -u origin main


## problem 1
C:\Users\shubhi\Desktop\INTERVIEW>git push -u origin main
fatal: unable to access 'https://github.com/Shubhanjali01/INTERVIEWS.git/': Recv failure: Connection was reset

- After switch of college proxy and connected to phone 

C:\Users\shubhi\Desktop\INTERVIEW>git push -u origin main

remote: Permission to Shubhanjali01/INTERVIEWS.git denied to divStriver99.

fatal: unable to access 'https://github.com/Shubhanjali01/INTERVIEWS.git/': The requested URL returned error: 403

### option 1 solution 
Option 1: Change Git Remote URL to SSH


# Check current remote
git remote -v

# Change remote to SSH instead of HTTPS
git remote set-url origin git@github.com:Shubhanjali01/INTERVIEWS.git

# Push again
git push -u origin main


**Error**
# Check current remote
git remote -v

# Change remote to SSH instead of HTTPS
git remote set-url origin git@github.com:Shubhanjali01/INTERVIEWS.git

# Push again
git push -u origin main

C:\Users\shubhi\Desktop\INTERVIEW>git push -u origin main

ERROR: Permission to Shubhanjali01/INTERVIEWS.git denied to Reah99.
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

## Option 2: Configure Git to use correct GitHub user
