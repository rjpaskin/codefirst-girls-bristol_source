---
title: Ruby and Git
---

In order to save to github you'll need a program called Git on your
laptop. To make Git easier we'll be using a program called gitgit.
To run gitgit you need Ruby installed, so in this step we'll install
that too.

### On Windows

On Windows the guys at [Rails Installer](http://railsinstaller.org/en) have put together a single package that contains both Ruby and Git. We're going to use that to get both on your laptop.

{% exercise %}
If you are on Windows (and haven't done so already):
* Download and install [Rails Installer](http://railsinstaller.org/en)
{% endexercise %}

### On a Mac

Macs come with Ruby already installed, so you don't have to worry about
getting Ruby!

To install git we're going to use a tool called [Homebrew](http://brew.sh/), which helps install open source software to a Mac.

{% exercise %}
* Open `Terminal` (Applications > Utilities > Terminal).
* Follow the installation instructions on the [Homebrew site](http://brew.sh/). It will ask you to copy and paste something like:

<pre><code>ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"</code></pre>

into the Terminal. (You should check this, as the precise instructions might have changed.)

* Once homebrew in installed type the following into the Terminal:

      brew install git
{% endexercise %}

### Tell Git who you are

Since Git (and Github) allows more than one more person to collaborate on a project (indeed, that's one of its big draws), you'll need to tell Git your name and email so that it can tag all your work.

{% exercise %}
1. Open *Terminal* or *Command Prompt with Ruby on Rails*
2. Type the following commands, taking care to substitute **your** name and email address (use the same one as you use with Github) - don't include the dollar ($) sign:

<pre><code>$ git config --global user.name 'My Name'
$ git config --global user.email my@email.com</code></pre>

If everything works, you should see nothing (which is the convention with Unix terminals - only when an error occurs will you see anythin). To check that Git has remembered you, you can enter the following into the command line:

<pre><code>$ git config --list</code></pre>

and you should see something like this (other lines may be present, don't worry about them):
<pre><code>user.name=My Name
user.email=my@email.com</code></pre>
{% endexercise %}
