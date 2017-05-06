# RWD: Git Exercise

This exercise designed to help you become familiar with the steps you'll need to follow to work with the RWD codebase after the migration from SVN to Git.

## Steps

1. Fork the repository

    A *fork* is a personal copy of the repository. This allows you to freely change your own repository without changing the original repository. The process of creating a fork is done through GitHub. If you are not familiar with this process, review the documentation to [Fork a Repo](https://help.github.com/articles/fork-a-repo/).

2. Clone the repository

    Once you've created your *fork* you'll want to *clone* the repository. This will download a working copy of the repository to your local machine. For more details, you may follow the steps for [cloning a repository](https://help.github.com/articles/cloning-a-repository/) outlined in the documentation.

3. Create a branch

    While you can work directly on the `master` branch, it's best practice to do your work on a separate branch. This is often called a *feature* branch. You can create and switch to a branch by running:
    
        git checkout -b feature-branch-name

4. Commit your work

    Once you've made your feature branch, do some work and make at least two commits to become familiar with the `git add`, `git commit`, and `git status` commands.

5. Push to your work

    Once you've made your commits you should push your work back to your *forked* repository on GitHub. You can do so by running:
    
        git push origin feature-branch-name

6. Open a Pull Request

    You should now see your feature branch on GitHub. Next open a pull request for your feature branch to be merged into the `master` branch of the *parent repository*. We will use Pull Requests to not only facilitate code merges, but also the code review process. For more details, review the documentation for [creating a Pull Request](https://help.github.com/articles/creating-a-pull-request/)


## Extra Steps

### Setup your SSH Keys

If you haven't already, you should follow the steps to generate an SSH key for your GitHub account. This will save you time by not having to continually type your GitHub credentials when running Git commands. You may follow the documentation for [connecting to GitHub with SSH](https://help.github.com/articles/connecting-to-github-with-ssh/) to create and add an SSH key to your GitHub account.

### Add an `upstream` remote

Over time your forked repository will become behind the parent repository. To pull changes from the parent repository you can setup an additional *remote* to reference the parent repository. A common name for this remote is `upstream`.

To create this upstream remote you can run:

    git remote add upstream ssh:something

After doing so you can reference the parent repository as `upstream`. For example, to pull the recent changes from `master` branch of the parent repository to your local copy, you can run:

    git pull upstream master
