#### Question 1

#### Step 1: Initialize the repository

mkdir my-demo-repo
cd my-demo-repo
git init

#### Step 2: Create and commit the initial file

echo "Line 1: Initial Content" > demo.txt
git add demo.txt
git commit -m "Initial commit with demo.txt"

#### Step 3: Modify the file and commit the changes

echo "Line 2: Added second line" >> demo.txt
git add demo.txt
git commit -m "Added second line to demo.txt"

#### Step 4: Modify the file without staging

echo "Line 3: Added third line" >> demo.txt

#### Step 5: Find commit hashes

git log --oneline

#### Step 6: Compare a specific commit to the staging area

git diff <commit_hash> #### Replace <commit_hash> with the hash of the earlier commit (e.g., def456)

<!-- Question 2 -->

#### Question 2

#### Step 1: Initialize a repository

mkdir my-release-demo
cd my-release-demo
git init

#### Step 2: Create initial file and commit for version 1.0.0

echo "Project: Stable Release 1.0.0" > release.txt
git add release.txt
git commit -m "Initial stable release 1.0.0"

#### Step 3: Create a tag for version 1.0.0

git tag v1.0.0

#### Step 4: Modify the file and commit for version 1.1.0

echo "Update: Added new features for 1.1.0" >> release.txt
git add release.txt
git commit -m "Added features for release 1.1.0"

#### Step 5: Tag version 1.1.0

git tag -a v1.1.0 -m "Release version 1.1.0 with new features"

#### Step 6: Modify the file and commit for version 2.0.0

echo "Update: Major overhaul for release 2.0.0" >> release.txt
git add release.txt
git commit -m "Major overhaul for release 2.0.0"

#### Step 7: Tag version 2.0.0

git tag -a v2.0.0 -m "Release version 2.0.0 with major changes"

#### Step 8: List all tags

git tag

#### Step 9: Push tags to remote

git remote add origin <repository_url> #### Replace <repository_url> with the actual URL
git push origin --tags

#### Step 10: Show details of specific tags

git show v1.0.0
git show v1.1.0
git show v2.0.0
