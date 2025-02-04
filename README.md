# InMOS Website Source

<!-- [![Github pages](https://github.com/m2lines/website-source/workflows/github%20pages/badge.svg?branch=master)](https://github.com/m2lines/website-source/actions) -->

This repo contains the source code for the InMOS website.
The site is built upon [M²LInES project website](https://m2lines.github.io/) and uses the [Hugo](https://gohugo.io/) framework.
The source files are written in markdown.
A [GitHub workflow](https://github.com/inmos-obvi/inmos-obvi.github.io/blob/master/.github/workflows/build-and-deploy.yaml) is configured to automatically build and deploy the website to <https://inmos-obvi.github.io/> whenever the `master` branch of this repo is updated.

## Instructions for updating this site

To update the site, you need to change the source files on the `master` branch of this repository.
There are two ways to do this.

### Easy Way: Edit on GitHub

You can edit the source files directly on GitHub from your browser.
To do this, navigate to the `content` folder and click the edit button (little pencil symbol).
Make your changes in the editor.
When you are done, you can either "Commit directly to the `master` branch" or "Create a new branch for this commit and start a pull request".
A direct commit is appropriate for a minor change.
A pull request is best if you want your changes to be reviewed and approved by the rest of the team.
This method only allows you to update one page at a time.

### Hard Way: Edit Locally

You can also clone this repository, make local changes, and then push them.
This is better for larger changes that involve multiple files and may need debugging.
<!--
#### Pre-commit
We use pre-commit to check file changes before they are pushed. You can download and install `pre-commit` using this [tutorial](https://pre-commit.com)

Basic git workflow
```bash
git clone git@github.com:m2lines/m2lines.github.io.git
cd m2lines.github.io
# edit files with your text editor
git add [new or modified files]
git commit -m '<your commit message>'
git push origin master
```
-->
If you want to make a large change, it may be best to discuss it first via pull request.
In that case you would want to create a new branch, push your branch to GitHub, and open a PR.
The GitHub docs on [creating a pull request](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request) are a useful reference here.

You can also build the website locally on your own computer.
This can be useful for debugging.
To do this, you need to first [Install Hugo](https://gohugo.io/getting-started/quick-start/).
You can then use the Hugo command line tools to do stuff like
```bash
hugo new content/<name of your page>.md # create a new page
hugo server -D # serve the website on http://localhost:1313/.
```

<!--
### Updating Tags
Member interests are defined in the form of tags which can link to personalized landing pages.
Example for adding tag to a member and giving it a custom landing page:
```
---
# the <user>.md
tags: [A, B, C]
---
```
Define the custom landing pages under `content/data/tag_links.yml`:
```
A: url-1
B: url-2
C: url-3
```
-->
