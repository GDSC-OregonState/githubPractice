# githubPractice

## Steps to Fork and Clone a Repository

### Step 1: Fork the Repository
Forking a repository allows you to create your own copy of the project under your GitHub account. This is helpful when you want to make changes to the code without affecting the original project.

1. **Visit the Organization's Repository**
   - Navigate to the repository of the organization that you want to fork. For example, `https://github.com/ORG_NAME/REPO_NAME`.

2. **Fork the Repository**
   - In the upper-right corner of the repository page, you’ll see a `Fork` button. Click it.
   - GitHub will create a copy of the repository under your account. The new repository will have the same name as the original, but it will now be located at `https://github.com/YOUR_USERNAME/REPO_NAME`.

### Step 2: Clone the Forked Repository
Once the repository has been forked, you can clone it to your local machine to work on it.

1. **Navigate to Your Forked Repository**
   - After forking, go to the repository under your GitHub profile: `https://github.com/YOUR_USERNAME/REPO_NAME`.

2. **Get the Repository URL**
   - On your forked repository page, click the green `Code` button, and copy the repository URL.
     - You can choose between HTTPS or SSH.
     - Example HTTPS URL: `https://github.com/YOUR_USERNAME/REPO_NAME.git`
     - Example SSH URL: `git@github.com:YOUR_USERNAME/REPO_NAME.git`

3. **Open a Terminal or Command Line**
   - Navigate to the directory where you want to clone the repository.
   
4. **Clone the Repository**
   - Use the `git clone` command followed by the copied URL to clone the repository:
     ```bash
     git clone https://github.com/YOUR_USERNAME/REPO_NAME.git
     ```
   - If you are using SSH:
     ```bash
     git clone git@github.com:YOUR_USERNAME/REPO_NAME.git
     ```

5. **Navigate into the Cloned Repository**
   - Change to the directory of the cloned repository:
     ```bash
     cd REPO_NAME
     ```

### Step 3: Sync with the Original Repository (Optional)
To keep your fork updated with the latest changes from the original repository, you'll want to add a remote pointing to the original repo (known as `upstream`).

1. **Add Upstream Remote**
   - Inside your cloned repository, add the original repository as an `upstream` remote:
     ```bash
     git remote add upstream https://github.com/ORG_NAME/REPO_NAME.git
     ```
   - If you are using SSH:
     ```bash
     git remote add upstream git@github.com:ORG_NAME/REPO_NAME.git
     ```

2. **Fetch the Latest Changes from Upstream**
   - To update your fork with any new changes made to the original repo:
     ```bash
     git fetch upstream
     ```

3. **Merge the Changes into Your Fork**
   - Merge the latest changes from the upstream repository into your local fork:
     ```bash
     git merge upstream/main
     ```
   - Replace `main` with the appropriate branch name if the repository uses a different default branch.

### Step 4: Start Working on the Project
Now that you've cloned the repository, you can start working on the project. You can create branches, make changes, and push them to your forked repository.

To push changes:
```bash
git add .
git commit -m "Your commit message"
git push origin main
