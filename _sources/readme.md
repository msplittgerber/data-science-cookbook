# The Data Science Cookbook

This repository is a collaborative project created for the purpose of learning about Git and GitHub, with special focus on collaborative workflows.

Each participant contributes to our collaborative cookbook by providing a single recipe of some food that he or she likes. The goal is to learn how to use Git and GitHub effectively, while also creating a useful resource for everyone involved.

Every time a recipe is merged into `main`, the cookbook is automatically built and deployed as a Jupyter Book using GitHub Actions. The cookbook is available at: https://msplittgerber.github.io/data-science-cookbook

[![Deploy Jupyter Book](https://github.com/msplittgerber/data-science-cookbook/actions/workflows/deploy.yml/badge.svg)](https://github.com/msplittgerber/data-science-cookbook/actions/workflows/deploy.yml)

The idea and setup of this project were originally created by Till Schwörer.


# Contribution Guidelines

## Initialization

- Each course participant will be added as a **collaborator** to this repository. GitHub then sends you an **invitation by email**, which you need to **accept within 7 days**. You can also see the invitation on this repository's page when you are logged in.
- **Clone the repository** to your local machine:
  `git clone https://github.com/msplittgerber/data-science-cookbook.git`

Please do all steps with Git on your own computer, not by editing files directly on the GitHub website.

## Adding a recipe

- **Branch**: Create a branch for your contribution and switch to it. Name it after your recipe, e.g. `git switch -c pasta`. All your changes are made inside this branch.
- **Develop**: Inside the folder `recipes/2026-winter/`, create a subfolder named after your recipe (e.g. `recipes/2026-winter/pasta/`). Copy the file `template/recipe.md` into your folder and fill it with life: ingredients, cooking instructions, cooking time, and personal hints and tricks. The template is a guide; feel free to adapt it.
- **Naming rules**: folder names in lowercase with hyphens instead of spaces (e.g. `chocolate-chip-cookies`). The recipe file is always called `recipe.md`. Image file names must not contain spaces (e.g. `image.jpg`).
- **Image** (optional, but nice): store it in your recipe folder and link it from your `recipe.md` with `![Short description](image.jpg)`. Please use **your own photo** (the cookbook is a public website, so no images copied from other websites) and **resize it to less than 1 MB** before committing.
- **Only change your own folder.** Do not edit other recipes, `_toc.yml`, or this README. The table of contents is generated automatically.
- **Commit**: Commit your changes regularly with descriptive commit messages, e.g. `git commit -m "Add ingredients for pasta"`. Each recipe should have **at least three commits**. Check with `git status` what you are about to commit before using `git add .`.
- **Push**: Push your branch to GitHub. The first time set the origin (your branch on github), e.g. use `git push -u origin pasta`. For follow-up pushes, `git push` is enough.
- **Pull request**: Open your branch on GitHub and create a pull request into the `main` branch. In the right sidebar, request your two assigned reviewers under "Reviewers".

## Review Process

- **Pull requests** need **at least 2 approvals** before they can be merged into `main`. Conversely, each participant reviews **2 pull requests** of other participants.
- **Reviewers** check for completeness and formal correctness (Does the image show? Are quantities and times given?), but can also ask for more personal touches, images, or additional hints and tricks. Don't treat the review as a mere formality: serious code reviews make a big difference, and so do serious recipe reviews. Comment directly on specific lines in the "Files changed" tab, then use "Review changes" to **Approve** or **Request changes**.
- **Recipe authors** consider the feedback carefully and either implement the requested changes or discuss them with the reviewers. To update your pull request, simply commit and push to the same branch again; the pull request updates automatically.
- **Merging**: once your pull request has **at least two approvals**, you merge it yourself with the "Merge pull request" button. Afterwards, your recipe appears on the cookbook website within a few minutes.
- **Clean up**: after merging, update your local repository:
  `git switch main`, then `git pull`, then e.g `git branch -d pasta` (use your own branch name).
- **Conflicts**: since everyone works in a separate folder, conflicts are unlikely. Should a merge conflict arise, resolve it as discussed in class.
