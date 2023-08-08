**Day 1
Open Source Contribution | Bootcamp**
-Issues
Issues are just tasks. They might be bugs, suggestions, or features. To experience the issue yourself, you can check the "Steps to reproduce"
The labels like- 'good first issue', 'bug', 'bounty' etc. are put by the maintainer of the repository. Unless it's, a big organization, do not wait for the issue to be assigned to you, if you feel you can do it, start working on it, and create the pull request (PR).
-Creating an issue
Go to the "Issues" tab, and click on new issue. Now, depending on the maintainers, you might or might not have 'templates' for the issues. The templates are stored in github/ISSUE_TEMPLATE
-Solving an issue
Create your own copy by clicking on fork. Solve the issue in that copy, and submit a pull request/merge request with the proper description. Write "fixes #[issue_no.]" in the first line and include some text, screenshots, etc. GitHub will automatically link your pull request to the issue. 

**Day 2
Git Branches and Pull Requests** 
After getting in the main branch, type “git checkout -b [new-branch-name]” e.g., git checkout -b “fix/typo-homepage”
The above command will create a new branch. Make changes in this branch, and type “_git add ._” then “_git commit -m [“one-line-description”]_”. Then _git push._ After this branch is created, open a pull request with main -> your_branch. Here you can provide all the details of your PR including the screenshot, type, tests,steps and most importantly- fixes#76 
The title of your PR should follow the conventions and pass the automated tests. Use fix:[description] or feat:[description]
If everything goes well, and your tests are passed, then the maintainer can merge your pull request if they feel it’s right.
If you want to create more branches, use _git switch main_, _git pull_ and then do the _git checkout -b branchname_. Never accidentally create a branch from branch.

**Day 3
Advance Git and Open Source Contribution**
Fork the repo to your account, go to your forked repo, click on code, copy the http link. Open the desired folder in your PC and type _git clone [link]_ in the cmd prompt. Then open your project in your machine, and set it up locally, e.g. yarn, yarn start, etc. 

Then create a new branch _git checkout -b “feat/new_feature_name” “git add .” git commit, git push_ etc. And also, there is something called gitignore, whatever you put in this folder, it’s not pushed to github as a part of your PR, code : npx gitignore Node.
Suppose there is an original repository called OG, then you create a copy of it by forking, then you create a copy of it on your local system. Now you create a branch on your local system, and the same branch is created on your forked repository. Then you merge your forked repo’s new branch, with the OG repo’s main branch. 
In this entire process, your local machine has no access to the OG repo, so whatever changes are made in the OG repo, can’t be reflected in your personal copy on your local system. In order to achieve that, go to your local code’s main using git switch main type the following “_git remote add OG [https link of the OG repo]_”, this will link the OG repo to your local environment. Then use _git pull OG main_, or _git fetch –all_. Then you can use _git push_ to push this code to your forked repo’s main branch.

**Day 4
Merge Conflicts and Doubt Clearing Session**
Suppose Issue1: Change a on Line32
And Issue2: Change b on Line32
If X contributes to Issue1, submits a PR, and gets his branch merged. And in the meanwhile, Y forked the main branch before X’s contribution, and submits his PR solving Issue2. Now a merge conflict will arise. 
So Y will have to examine how the conflict can be resolved without breaking any code. So Y should run git pull OG main in the local environment branch. Now Y will logically resolve the merge conflict. After this Y can run/type:   _git add . 	 git rebase –continue	git status	git push -f_

Reverting a commit
To get commitID use _git log –oneline_
To revert it use  _git revert [commitID]_
