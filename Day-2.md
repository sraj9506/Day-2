### Git Project (2.5 Hours)

#### Project Setup (15 minutes)

Install Git:

![](.//media/image1.png)

![](.//media/image2.png)
Set Up Git:

 Configure your Git username and email for that first we have to create
 an account on github and then set Author and Email.

![](.//media/image3.png)

Create & Clone a GitHub Repository:

Go to GitHub and create a new repository named website-project.

Clone the repository to your local machine .

Here we need to type our github repository url along with the command.

![](.//media/image4.png)

Initialize the Project:

Navigate to the project directory.

![](.//media/image5.png)

Create initial project structure .

![](.//media/image6.png)

![](.//media/image7.png)

![](.//media/image8.png)

Commit and push the initial project structure.

Here (.) indicates that we are adding all files of this folder to git
staging environment.

![](.//media/image9.png)

Here -m is useful for giving comment to the commit which we done.

![](.//media/image10.png)

Here main is a branch name and origin refers to the our repository.

![](.//media/image11.png)

Exercise 1: Branching and Basic Operations (10 minutes)

Create a New Branch:

Checkout is used for switching the branch but when we passed -b option
then if that branch is not exist then it will create it and then switch
it and also the newly created branch is initialized based on currently
active branch.

![](.//media/image12.png)

Add new Page:

![](.//media/image13.png)

![](.//media/image14.png)

![](.//media/image15.png)

![](.//media/image16.png)

![](.//media/image17.png)

#### Exercise 2: Merging and Handling Merge Conflicts (15 minutes)

Create Another Branch:

First we switched to the main branch because we want to create the
branch based on main branch.

![](.//media/image18.png)

Now we create one more branch.

![](.//media/image19.png)

Update the Homepage:

![](.//media/image20.png)

![](.//media/image21.png)

![](.//media/image23.png)

Create a Merge Conflict:

Modify index.html on the featured/add-about-page branch.

![](.//media/image24.png)

![](.//media/image25.png)

![](.//media/image26.png)

Merge and Resolve Conflict:

Attempt to merge featured/add-about-page and featured/update-homepage
into main.

![](.//media/image27.png)

Here you can see that conflict is arises now we need to resolve it.

For that we have to first configure the git mergetool which is only
available after merge conflict arise .

![](.//media/image28.png)

Here we passing vimdiff as a tool for resolved merge conflict. There are
plenty of other editor also available for resolve conflicts.

Below is the screen of vimdiff editor. Here top left panel is the
content of already merged branch , top middle contains content of file
which has conflict but without any merge and top right is the content of
branch which triggers conflict when we try to merge that branch.

And in the bottom part we has merged content of both branch where head
refers already merged and featured/update-homepage refers a content
which we try to merge now.

![](.//media/image29.png)

![](.//media/image30.png)

#### Exercise 3: Rebasing (10 minutes)

Rebase a Branch:

Rebase feature/update-homepage onto main.

![](.//media/image31.png)
In below image you can see that now this branch has about page which is
result of rebase, here main branch is totally replicated in
featured/update-homepage.

![](.//media/image32.png)

![](.//media/image33.png)
Exercise 4: Pulling and Collaboration (10 minutes)

Pull Changes from Remote:

Ensure the main branch is up-to-date.

![](.//media/image34.png)

Simulate a Collaborator's Change:

Make a change on GitHub directly.

![](.//media/image35.png)

Pull Collaborator's Changes:

Pull the changes made by the collaborator.

![](.//media/image36.png)

####  

#### 

####  Here we can see that there is one insertion in index.html.

![](.//media/image37.png)

#### Exercise 5: Versioning and Rollback (15 minutes)

Tagging a Version:

Tag the current commit as v1.0. Here we use -a option to denote
annotated tag rather than lightweight tag because annotated tag provide
additional metadata such as name,email,etc.

![](.//media/image38.png)

Make a Change that Needs Reversion:

![](.//media/image39.png)

![](.//media/image40.png)

Revert to a Previous Version:

Here HEAD refers to the most recent commit.

![](.//media/image41.png)

![](.//media/image37.png)

Alternatively, reset to a specific commit (use with caution):

![](.//media/image42.png)

Here we use specific commit hash to reset our branch to that commit. We
can find commit hash in log which is shown extra activities part.

Difference between revert and reset is revert is make new commit while
reset change head pointer to specified commit and delete the commits
which is after made by specified commit. That's why it's risky.

![](.//media/image25.png)

![](.//media/image43.png)

Here we reset the HEAD pointer in our local repository but in remote
repository HEAD pointer is at forward position so we need to forced push
for that. That's why we use -f option with push command.

Extra Activities (10 minutes)

Stashing Changes:

Make some local changes without committing.

![](.//media/image44.png)

Stash the changes, Here after stashing we can moved in another branch
without commit and later on apply it when we needed and also after the
stashing we can not

see updated content in our file until and unless we apply the stash.

![](.//media/image45.png)

Apply the stashed changes.

![](.//media/image46.png)
Viewing Commit History:

![](.//media/image47.png)we use --oneline option for show only
commit message and commit hash otherwise it will give detailed output.

Cherry-Picking Commits:

Here we create a new branch and cherry-pick our first commit, which
means a changes which is saved on first commit is automatically applied
on newly created branch.

![](.//media/image48.png)

Here we also faced merge conflict so first we resolve it then continue
the cherry pick.

![](.//media/image49.png)
Interactive Rebase:

Here we go to 3 commit back and apply it to the main branch so it will
cause merge conflict , but after resolve it we able to do rebase the
branch main and it will erase all commit which is made after that
applied commit.![](.//media/image50.png)
Collaborative Blogging Platform

#### Objective:

You will work on a project to collaboratively develop a simple blogging
platform. You will practice various Git concepts including branching,
merging, handling merge conflicts, rebasing, pulling, versioning,
rolling back changes, stashing, and cherry-picking commits. The project
is designed to be completed in 1.5 Hours

Create a GitHub Repository:

![](.//media/image51.png)

Initialize the Project:

![](.//media/image52.png)

![](.//media/image53.png)

#### 

#### 

#### Exercise 1: Branching and Adding Features (20 minutes)

Create a New Branch for Blog Post Feature:

![](.//media/image55.png)

Add a Blog Post Page:

![](.//media/image56.png)

![](.//media/image57.png)

![](.//media/image58.png)

#### 

#### 

#### Exercise 2: Collaborating with Merging and Handling Merge Conflicts (25 minutes)

Create Another Branch for Author Info:

![](.//media/image59.png)

Add Author Info to Blog Page:

![](.//media/image60.png)

![](.//media/image61.png)

Create a Merge Conflict:

![](.//media/image62.png)

![](.//media/image63.png)
![](.//media/image64.png)

Merge and Resolve Conflict:

![](.//media/image65.png)

![](.//media/image66.png)

Exercise 3: Rebasing and Feature Enhancement (25 minutes)

Rebase a Branch for Comment Feature:

![](.//media/image68.png)

Add Comment Section:

![](.//media/image69.png)
![](.//media/image70.png)

#### 

#### 

#### Exercise 4: Pulling and Simulating Collaboration (20 minutes)

Pull Changes from Remote:

![](.//media/image71.png)

Simulate a Collaborator's Change:

![](.//media/image72.png)

Pull Collaborator's Changes:

![](.//media/image73.png)

#### 

#### Exercise 5: Versioning and Rollback (30 minutes)

Tagging a Version:

![](.//media/image74.png)

Make a Change that Needs Reversion:

![](.//media/image75.png)

![](.//media/image76.png)

Revert to a Previous Version:

![](.//media/image77.png)

![](.//media/image78.png)

Extra Activities (25 minutes)

Stashing Changes:

![](.//media/image79.png)

![](.//media/image80.png)

Viewing Commit History:

![](.//media/image81.png)

Cherry-Picking Commit

![](.//media/image82.png)

Interactive
Rebase![](.//media/image83.png)
