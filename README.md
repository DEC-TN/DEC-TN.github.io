# ERC-TN.github.io
Website for erc-tn.org

**Set Up Your Local Environment**

If you don't have a Github account, go ahead and create one. Ping me with your Github user and I'll add you to the repo.

Mac/Linux
  * If on Mac, install [homebrew](https://brew.sh). If on Linux, skip this step.
  * If on Mac, open a terminal and run the command `brew install jekyll`, if on Linux use the package manager `sudo apt-get install jekyll` for Debian flavors, for example.
  * Next, run `brew install git` or `sudo apt-get install git` depending on Mac or Linux.
  * After it is installed, click the "Code" button above to get the SSH url to checkout the project from.
  * From your terminal, type `cd ~` to return to your home directory.
  * Run `git clone git@github.com:ERC-TN/ERC-TN.github.io.git erc-tn`.
  * Once it has finished, run `cd erc-tn`.
  * To start the server, run `bundle exec jekyll serve` to start Jekyll, or `bundle exec jekyll serve --watch` to start it in watch mode where it updates as soon as files are changed.
  * Navigate to http://localhost:4000 and see it in action.
  
**Theming**

Jekyll uses [SASS](https://sass-lang.com) to preprocess stylesheets. It is a wonderful thing to not have to edit a million slightly differing stylesheets for different pages anymore.

All styles can be found in the `/assets/css` directory. Note that SASS compiles CSS by discarding brackets and ONLY using indentation to determine nesting, so be aware that indentation is very important.

**Adding New Layouts**

Each page will use the `default.html` layout by... default. More can be added and used as necessary, just copy `default.html` and add/subtract whatever you want from it.

**Adding New Pages**

Each page lives as a Markdown file in the base directory. Good practice would be to copy `about.md` and change the text however you want it. You can change the layout by setting the `layout: <name>` parameter at the top of page. To add the page to the main menu, add `page-category: menu` in there as well.
