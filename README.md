# Repository1
Some text

## Another header

Some text

### Third header

steps:

step 1: Open index.html in the browser

step 2: Watch the video tutorial through the link below
    (Lorem ipsum blahblahblah)

# TypeScript steps made

step 1 ran **npm init -y**     // creates package.json file this define the project's dependencies and their exact versions. with this other developers cloning them or ME in the future will know which libraries I need to install.

step 2 ran **tsc --init**      // creates tsconfig.json configuration file in the project root, essentially setting up the rules and environment for the TypeScript compiler to build for the project.

step 3 create src folder to store .ts files

step 4 create index.ts file for testing

## How to run typescript codes *.ts files

Step 1: Open terminal
Step 2: ran **tsc**     //creates dist directory with the <filename>.js inside
step3: ran **dist/<filename>.js**     //make sure to add the directory first before the filename since it is configure in tsconfig that .js files created from tsc command will be created in the dist directory. This will run the program
step 4: ran tsc --watch     // ttells typescript to keep running in the background and recompile .ts files whenever changes are saved. No need for step 2. 

### How to create pull request from previous commits from the same branch

To create a Pull Request (PR) from a previous commit on your current branch, you cannot directly tell GitHub to "only look at the past." Instead, the standard and safest Git workflow is to create a brand-new branch pointing exactly at that older commit and push that new branch to GitHub.

## step 1: Find the Hash of the Older Commit

First, you need the unique ID (hash) of the specific commit you want to create the PR from.

Run this command to view your recent commit history:

git log --oneline

## step 2: Copy the 7-character hash of the commit you want (in this example, e5f6g7h).

Now, create a brand-new branch that starts exactly at that older commit. This leaves your current branch completely untouched.

git branch <new-branch-name> <commit-hash>

For example:

git branch pr-tsconfig e5f6g7h

## Step 3: Push the New Branch to GitHub

Switch to your newly created branch and push it up to your remote repository:

# Switch to the new branch
git checkout pr-tsconfig

# Push it to GitHub
git push origin pr-tsconfig

## Step 4: Open Your Pull Request on GitHub
1 Go to your repository page on GitHub.

2 You should see a yellow banner saying "pr-tsconfig had recent pushes x minutes ago".

3 Click the green "Compare & pull request" button next to it.

4 Set the base branch (usually main) and ensure the compare branch is your new pr-tsconfig branch.