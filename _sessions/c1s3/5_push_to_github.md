---
title: "Pushing to GitHub"
---

Git is a version control system. It allows you to keep the entire history of your code, and makes it easy to share and collaborate with others.

### Using Git

Using Git is really easy:

1. Set up a folder to be a _Git repo_. This tells Git to track all changes in that folder.
2. After you've made some changes, save them into the repository.
3. Once you've saved the changes push them up to Github.

The first point is important: *Git works on a folder level*. It tracks all the changes you make to files within a given folder.

### Actually using Git

Actually using Git is a bit harder. It's a very powerful tool and pretty complex to get started with. To make things simpler, we're going to use a tool called `gitgit`.

To install gitgit open the command line and type the following:

    gem install gitgit

To see if this worked, type

    gitgit

You should see a list of gitgit commands something like this:

    $ gitgit
    Commands:
      gitgit help [COMMAND]  # Describe available commands or one specific command
      gitgit init            # Initialise a git repo
      gitgit lg              # Show your recent saves
      gitgit push            # Push your changes to github
      gitgit save            # Save you changes to the repo
      gitgit status          # See what changes you've made since you last save

If it didn't work, you might need to do

    sudo gem install gitgit

and type your password.

If in doubt, contact a teaching assistant!

### Using gitgit

To **make a folder into a git repository**:

    gitgit init

then follow the instructions. You'll only need to do this once for each folder you want to make into a repository.

After you've made some changes to your files and saved them, you can **save them into your repo** by typing:

    gitgit save

Finally, to push your code up to Github you can do

    gitgit push

Before you do this, you will need to setup your repo with Github.

### Setting up your repo with Github

Go to Github, login, and click "Create New Repo" in the top left hand corner.

![Creating a repo on Github](/assets/create_repo.png)

Follow the instructions, calling it something like `first_site`. **Do not** click the box which says 'Create a readme with this repository'. You'll get to a page when it'll describe how to get your code online. You want to follow the instructions for "Pushing an existing repository to Github".

### Pushing your code to Github

We will now set up your `first_site` folder to use git and push it up to Github.

{% exercise %}
1. Navigate to your first_site folder using `cd` and `ls`.
2. Make it into a git repo: `gitgit init`.
3. Save all the work you've done so far: `gitgit save`.
4. Log in to Github.
5. On Github create a new repository called 'first_site'. DO NOT click the box which says 'Create a readme'.
6. Copy and paste the instructions it gives you into the command line. You are 'Pushing an existing repository to Github'.
7. Go back to Github and refresh the page. You should see your code.
{% endexercise %}

### Publishing site using GitHub pages

You're now going to publish your `first_site` using [GitHub Pages](https://pages.github.com/).

To do this you need to push your website up to a branch called
`gh-pages`. You don't know about branches yet, but you can see them on
Github. Right now you'll just see a single branch called `master`.

You don't actually need to understand anything about branches at the
moment, as gitgit makes it really easy to publish as a Github page. Just
run

    gitgit publish

When you go to github you should now see a `gh-pages` option in the
branches dropdown.

The `gh-pages` branch is a signal to Github that you want your code to
be deployed as a website. You can find the URL of your website by
looking in your repository settings on GitHub.
