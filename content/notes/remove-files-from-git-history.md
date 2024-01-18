---
title: Remove files from Git history
date: 2024-01-18T12:05:00
description: A quick how to guide on how to remove data from a repository's history
tags: ['git', 'guide']
---

A note for myself because I know I'll probably do it again in the future...

I managed to accidently commited a text file to a repository and pushed it to GitHub 🤦🏽‍♂️

While it didn't contain any sensitive data, I still wanted to remove it from the repository's history. I found [this guide on GitHub](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository) and these are the exact steps I followed to resolve this issue.

1. Install [bfg via Homebrew](https://formulae.brew.sh/formula/bfg)
    ```zsh
    brew install bfg
    ```
2. Remove the file from the local repository and push this change to the GitHub repository
3. Clone the repository from GitHub to a new location on my machine
    ```zsh
    gh repo clone GITHUB_USERNAME_HERE/REPOSITORY_NAME_HERE
    ```
4. Ran the following command to remove the file from the repository's history
    ```zsh
    bfg --delete-files FILENAME_HERE_WITH_EXTENSION
    ```
5. Then I ran these commands together (This was what was recommended after running the command above)
    ```zsh
    git reflog expire --expire=now --all && git gc --prune=now --aggressive
    ```
6. Force push the changes to GitHub
    ```zsh
    git push --force
    ```

The file should now be removed from GitHub and you should see a new commit message with no changes made.
