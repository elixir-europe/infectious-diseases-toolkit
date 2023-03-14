---
title: Working with git
---


## Forking - branching - changing - pushing - PR

This is a general workflow in how to work on your own fork (copy) of the Infectious Diseases Toolkit repo and request changes through a pull request:
NOTE: if you already did these steps in the past, start from the `git fetch upstream` command. 

- Make a fork of this repository, using the fork button.
- Open a terminal and clone your fork using:
    ```
    git clone git@github.com:USERNAME/infectious-diseases-toolkit.git
    cd infectious-diseases-toolkit
    ```
    NOTE: Make sure you clone the fork and not the original elixir-europe/infectious-diseases-toolkit one.
- Keep your fork up to date (IMPORTANT!).
    ```
    git remote add upstream https://github.com/elixir-europe/infectious-diseases-toolkit.git
    git fetch upstream
    git checkout main (if you are not already on the main branch, check with `git branch`)
    git pull upstream main
    ```
- Create a new branch named after your feature/edit.
    ```
    git checkout -b 'FEATURE_NAME'
    ```
- Make the changes you want to make using an editor of choice
- Save.
- Open terminal and stage your changes:
    ```
    git add .
    ```
- Committing changes
    ```
    git commit -m "Changing the tool-resource file"
    ```
- Pushing you changes to your fork
    ```
    git push origin 'FEATURE_NAME'
    ```
- Go to [https://github.com/elixir-europe/infectious-diseases-toolkit](https://github.com/elixir-europe/infectious-diseases-toolkit) and click on *Compare & pull request*
- Open the pull request an describe your changes.
- Wait for review by other editors. Editors that are responsible for the sections you make changes to will be assigned as reviewer automatically.

## The advantage of working locally: previewing your changes through your web browser

The website is build on GitHub using Jekyll, a simple, static site generator based on ruby. When you have a local copy cloned onto your computer, it is possible to generate the website based on this repo. This makes it possible to preview changes live, every time you save a file from within the GitHub Infectious Diseases Toolkit repo. Follow these steps to deploy the website based on your local clone (copy) of the Infectious Diseases Toolkit repo:

Make sure you have cloned the Infectious Diseases Toolkit repo:

    git clone git@github.com:USERNAME/infectious-diseases-toolkit.git
    cd Infectious Diseases Toolkit


To run the website locally, you can either use [Docker](https://www.docker.com/) or use Jekyll directly after installing various dependencies.

### Run using Docker

1. If not already installed on your machine, install Docker. From the root of the ``infectious-diseases-toolkit`` directory, run:
    ```
    docker run -it --rm -p 4000:4000 -v $PWD:/srv/jekyll jekyll/jekyll:3 /bin/bash -c "chmod -R 777 /srv/jekyll && bundle install && bundle exec jekyll serve -w - --host 0.0.0.0 --livereload"
    ```
This will start the docker container and serve the website locally.

### Run using Jekyll directly

1. If not already present on your machine, install ruby. Note that incompatibility issues may arise with ruby 3.0.0 (released 25.12.20) or newer versions.


1. Install Jekyll
If you have never installed or run a Jekyll site locally on your computer, follow these instructions to install Jekyll:
   * Install Jekyll on MacOS/Ubuntu/Other_Linux/Windows: [https://jekyllrb.com/docs/installation/](https://jekyllrb.com/docs/installation/)

1. Install Bundler and Jekyll

    ```
    gem install jekyll
    ```

1. Install dependencies

    ```
    bundle install
    ```

1. deploy website

    ```
    bundle exec jekyll serve
    ```

Additional information can be found at the following link: [https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll)
