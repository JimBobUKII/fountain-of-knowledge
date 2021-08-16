# Forking a repository
A fork is a copy of a repository. Forking a repository allows you to freely experiment with changes without affecting the original project.

## About forks
Most commonly, forks are used to either propose changes to someone else's project or to use someone else's project as a starting point for your own idea. You can fork a repository to create a copy of the repository and make changes without affecting the upstream repository. For more information, see "Working with forks."

### Propose changes to someone else's project
For example, you can use forks to propose changes related to fixing a bug. Rather than logging an issue for a bug you've found, you can:

- Fork the repository.
- Make the fix.
- Submit a pull request to the project owner.

### Use someone else's project as a starting point for your own idea.
Open source software is based on the idea that by sharing code, we can make better, more reliable software. For more information, see the "About the Open Source Initiative" on the Open Source Initiative.

For more information about applying open source principles to your organization's development work on GitHub, see GitHub's white paper "An introduction to innersource."

When creating your public repository from a fork of someone's project, make sure to include a license file that determines how you want your project to be shared with others. For more information, see "Choose an open source license" at choosealicense.com.

For more information on open source, specifically how to create and grow an open source project, we've created Open Source Guides that will help you foster a healthy open source community by recommending best practices for creating and maintaining repositories for your open source project. You can also take a free GitHub Learning Lab course on maintaining open source communities.

## Prerequisites
If you haven't yet, you should first set up Git. Don't forget to set up authentication to GitHub from Git as well.

You might fork a project to propose changes to the upstream, or original, repository. In this case, it's good practice to regularly sync your fork with the upstream repository. To do this, you'll need to use Git on the command line. You can practice setting the upstream repository using the same octocat/Spoon-Knife repository you just forked.

- On GitHub, navigate to the octocat/Spoon-Knife repository.
- In the top-right corner of the page, click Fork.

## Cloning your forked repository
Right now, you have a fork of the Spoon-Knife repository, but you don't have the files in that repository locally your computer.

- On GitHub, navigate to your fork of the Spoon-Knife repository.
- Above the list of files, click  Code.
- To clone the repository using HTTPS, under "Clone with HTTPS", click . To clone the repository using an SSH key, including a certificate issued by your organization's SSH certificate authority, click Use SSH, then click . To clone a repository using GitHub CLI, click Use GitHub CLI, then click .
- Open Git Bash.
- Change the current working directory to the location where you want the cloned directory.
- Type git clone, and then paste the URL you copied earlier. It will look like this, with your GitHub username instead of YOUR-USERNAME:
    ```bash
    $ git clone https://github.com/YOUR-USERNAME/Spoon-Knife
    ```
- Press Enter. Your local clone will be created.
    ```bash
    $ git clone https://github.com/YOUR-USERNAME/Spoon-Knife
    > Cloning into `Spoon-Knife`...
    > remote: Counting objects: 10, done.
    > remote: Compressing objects: 100% (8/8), done.
    > remove: Total 10 (delta 1), reused 10 (delta 1)
    > Unpacking objects: 100% (10/10), done.
    ```

## Configuring Git to sync your fork with the original repository
When you fork a project in order to propose changes to the original repository, you can configure Git to pull changes from the original, or upstream, repository into the local clone of your fork.

- On GitHub, navigate to the octocat/Spoon-Knife repository.
- Above the list of files, click  Code.
- To clone the repository using HTTPS, under "Clone with HTTPS", click . To clone the repository using an SSH key, including a certificate issued by your organization's SSH certificate authority, click Use SSH, then click . To clone a repository using GitHub CLI, click Use GitHub CLI, then click .
- Open Git Bash.
- Change directories to the location of the fork you cloned.
  - To go to your home directory, type just cd with no other text.
  - To list the files and folders in your current directory, type ls.
  - To go into one of your listed directories, type cd your_listed_directory.
  - To go up one directory, type cd ...
- Type git remote -v and press Enter. You'll see the current configured remote repository for your fork.
    ```bash
    $ git remote -v
    > origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
    > origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
    ```
  - Type git remote add upstream, and then paste the URL you copied in Step 2 and press Enter. It will look like this:
  ```bash
  $ git remote add upstream https://github.com/octocat/Spoon-Knife.git
  ```
- To verify the new upstream repository you've specified for your fork, type git remote -v again. You should see the URL for your fork as origin, and the URL for the original repository as upstream.
    ```bash
    $ git remote -v
    > origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
    > origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
    > upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (fetch)
    > upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (push)
    ```
Now, you can keep your fork synced with the upstream repository with a few Git commands. For more information, see "Syncing a fork."

### Next steps
You can make any changes to a fork, including:

- Creating branches: Branches allow you to build new features or test out ideas without putting your main project at risk.
- Opening pull requests: If you are hoping to contribute back to the original repository, you can send a request to the original author to pull your fork into their repository by submitting a pull request.

## Find another repository to fork
Fork a repository to start contributing to a project. You can fork a repository to your user account or any organization where you have repository creation permissions. For more information, see "Permission levels for an organization."

If you have access to a private repository and the owner permits forking, you can fork the repository to your user account or any organization on GitHub Team where you have repository creation permissions. You cannot fork a private repository to an organization using GitHub Free. For more information, see "GitHub's products."

You can browse Explore to find projects and start contributing to open source repositories. For more information, see "Finding ways to contribute to open source on GitHub."
