# learning-Git

1. To double-check that Git is installed, type git `--version`:
``` bash
git --version

```

You should see output that looks something like this example:
<pre>
git version 2.38.1
</pre>

2. To configure Git, you must define some global variables: `user.name` and `user.email`. Both are required for you to make commits.

3. Set your name in Cloud Shell with the following command. Replace `<USER_NAME>` with the user name you want to use.

``` bash
git config --global user.name "<USER_NAME>"

```

4. Now, use this command to create a user.email configuration variable, replacing `<USER_EMAIL>` with your `e-mail address`:

``` bash

git config --global user.email "<USER_EMAIL>"

```
5. Run the following command to check that your changes worked:

``` bash
git config --list

```

## Set up your Git repository

Git works by checking for changes to files within a certain folder. We'll create a folder to serve as our working tree (project directory) and let Git know about it, so it can start tracking changes. We tell Git to start tracking changes by initializing a Git repository into that folder.

1. Create a folder named Cats. This folder will be the project directory, also called the working tree. The project directory is where all files related to your project are stored.

``` bash
mkdir Cats

```
2. Change to the project directory by using the `cd` command:

``` bash
cd Cats

```

3. Now, initialize your new repository and set the name of the default branch to `main`:

``` bash
git init --initial-branch=main
git init -b main

```
4. Now, use a `git status` command to show the status of the working tree:

``` bash
git status
```

Git responds with this output, which indicates that main is the current branch. (It's also the only branch.) So far, so good.

<pre>

OUTPUT:

On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
</pre>

5. Use an ls command to show the contents of the working tree:

``` bash
ls -a
```

## Create and add a file

1. Use a touch command to create a file named `index.html`:

``` bash
touch index.html
```
`touch` updates a file's last-modified time if the file exists. If the file doesn't exist, Git creates an empty file with that file name.

2. Now, use git status to get the status of the working tree:

``` bash
git status
```

Git responds by informing you that nothing has been committed, but the directory does contain a new file:

<pre>
No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

    index.html

nothing added to commit but untracked files present (use "git add" to track)
</pre>
