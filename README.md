# ERC-TN.github.io
Website for erc-tn.org

**Set Up Your Local Environment**

If you don't have a Github account, go ahead and create one. Ping me with your Github user and I'll add you to the repo.

Mac/Linux:
  * Create an SSH key:
    * Open a terminal and type `cd ~/.ssh`.
    * Then type `ssh-keygen -b 4096 -C "My Github Key"`.
    * In the prompt that appears, type `github`.
    * In the password fields that follow, just hit Enter to skip the password.
    * Once you see the neat ASCII art of your digital fingerprint, type `ssh-add github` to add your key.
    * Go into your Github account settings (Click your profile icon in the very top right, click "Settings").
    * Click the tab labelled "SSH and GPG Keys", click the green "New SSH Key" button at the top right.
    * Give a title to your key.
    * IMPORTANT! In your terminal, type `cat github.pub`. There should be a huge block of random characters.
    * Copy and paste the entire thing into the Key field and click "Add SSH Key".
    * It should appear in your list of keys.
  * If on Mac, install [homebrew](https://brew.sh). If on Linux, skip this step.
  * If on Mac, open a terminal and run the command `brew install jekyll`, if on Linux use the package manager `sudo apt-get install jekyll` for Debian flavors, for example.
  * Next, run `brew install git` or `sudo apt-get install git` depending on Mac or Linux.
  * From your terminal, type `cd ~` to return to your home directory.
  * Run `git clone git@github.com:ERC-TN/ERC-TN.github.io.git erc-tn`.
  * Once it has finished, run `cd erc-tn`.
  * To start the server, run `bundle exec jekyll serve` to start Jekyll, or `bundle exec jekyll serve --watch` to start it in watch mode where it updates as soon as files are changed.
  * Navigate to http://localhost:4000 and see it in action.
  
Windows:
  * I'll add instructions for Windows users when I get a PC to test on.
  
**Theming**

Jekyll uses [SASS](https://sass-lang.com) to preprocess stylesheets. It is a wonderful thing to not have to edit a million slightly differing stylesheets for different pages anymore.

All styles can be found in the `/assets/css` directory. Note that SASS compiles CSS by discarding brackets and ONLY using indentation to determine nesting, so be aware that indentation is very important.

**Adding New Layouts**

Each page will use the `default.html` layout by... default. More can be added and used as necessary, just copy `default.html` and add/subtract whatever you want from it.

**Adding New Pages**

Each page lives as a Markdown file in the base directory. Good practice would be to copy `about.md` and change the text however you want it. You can change the layout by setting the `layout: <name>` parameter at the top of page. To add the page to the main menu, add `page-category: menu` in there as well.

**Committing Changes**

So now you've got shiny new changes on your local, and you want to publish them to the live site. The safe method to do so is to create a branch with your changes and push it up to Github for review.

When you first cloned this repository, you started on branch `master` (not a slavery reference, but still problematic; unfortunately Github Pages currently only works for free on the master branch. I suspect that will change once they switch the default branch name from master to main). Open a terminal:
  * `cd ~/erc-tn`
  * `git checkout -b change/<a-brief-title>` switches to a new branch that is a duplicate of master
  * `git add .` will add everything you changed
  * `git commit -m "Write a description of why the changes were made"` will write the changes to your local branch
  * `git push origin <my-branch>` will push it back up to Github
  * In the repository, click Pull Requests
  * If you just pushed it up, there should be a little yellow box with your branch name, and a button to automatically create a Pull Request from it. If not, click "New Pull Request"
  * Find your branch and select it in the `compare: ` select list. Keep the `base: master` select list as-is
  * Once Github has done it's comparison, it should tell you it's ready for merging, go ahead and save the PR (Pull Request)
  * Let @patpluspun know that it's there and I'll review it and merge it if it's good, or suggest changes if it could use some work
  * Once it's merged, you have just started the journey to becoming a professional web developer
