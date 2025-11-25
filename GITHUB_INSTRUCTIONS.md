# How to Upload Your Project to GitHub

Follow these steps to publish your "Fault-Tolerant NoC Simulator" to GitHub.

## Prerequisite: Install Git
If you haven't installed Git yet, download it from [git-scm.com](https://git-scm.com/downloads) and install it.
To check if it's installed, run:
```bash
git --version
```

## Step 1: Create a Repository on GitHub
1.  Log in to your [GitHub account](https://github.com/).
2.  Click the **+** icon in the top-right corner and select **New repository**.
3.  **Repository name**: `fault-tolerant-noc` (or whatever you like).
4.  **Description**: "Simulation of Fault-Tolerant Task Mapping for Many-Core Processors".
5.  **Public/Private**: Choose Public (so your teacher can see it) or Private.
6.  **Initialize this repository with**: Leave all these unchecked (no README, no .gitignore) because we already made them locally.
7.  Click **Create repository**.

## Step 2: Push Your Code (Run these in your VS Code Terminal)

1.  **Initialize Git**:
    ```bash
    git init
    ```

2.  **Add all files**:
    ```bash
    git add .
    ```
    *(This stages all your files, including the `assets` folder and code)*

3.  **Commit the files**:
    ```bash
    git commit -m "Initial release: FTTM Simulator with Stress Tests and Comparison"
    ```

4.  **Link to GitHub** (Replace `<URL>` with the link from Step 1):
    *   Copy the URL from the GitHub page (it looks like `https://github.com/yourname/repo.git`).
    *   Run:
    ```bash
    git branch -M main
    git remote add origin <PASTE_YOUR_GITHUB_URL_HERE>
    ```

5.  **Upload (Push)**:
    ```bash
    git push -u origin main
    ```

## Step 3: Verify
Refresh your GitHub repository page. You should see:
-   Your beautiful `README.md` rendered with images.
-   Your code files.
-   The `assets` folder.

## Troubleshooting
-   **"Remote origin already exists"**: Run `git remote remove origin` and try adding it again.
-   **Authentication**: If it asks for a password, you might need to use a [Personal Access Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) if you don't have SSH keys set up.
