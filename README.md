<img width="250" src="https://design.neto.com.au/assets/themerepos5/storefront.jpg">

Store Front 2021 is a free theme for Neto based on the Free Theme "Store Front" available in the Neto Theme Store. The main difference is that Store Front 2021 is built on the latest Bootstrap 4, jQuery and our goal is for the latest skeletal updates to be included as well.

Work on this theme is being completed by volunteer's - no support or warranty is given. Use at your own risk. You are most welcome to contribute and provide bug fixes. 

`Please Note:` most of the work on this theme was completed by the team at [Neto E-commerce Solutions](http://neto.com.au) we are in no way claiming this as our original work. This repository was created to simply provide an updated version of the Store Front Theme.

## Table of contents

- [Installation](#installation)
- [Documentation](#documentation)
- [Testing](#testing)
- [Contribute](#contribute)
- [Creators](#creators)

## Installation

**Directly install**

To install the latest version of Store Front 2021 directly from this repository you simply need to upload the `src` directory from this repository into the `httpdocs/assets/themes` directory on your Neto website. You should also rename this new `src` directory to whatever you would like your custom theme to be named. You will want to have ran `npm run build` first so you have the compiled css. 

For the above, you will need FTP access to your Neto website, which you can request [here](http://forms.neto.com.au/design/requestftp.html).

## Documentation

Documentation for designers and developers can be found [here](https://developers.neto.com.au/).

As Skeletal is built almost entirely upon Bootstrap 4, the [Bootstrap documentation](https://getbootstrap.com/docs/4.1/getting-started/introduction/) is perhaps the most valuable source of documentation for a web designer who isn't looking to build complex functionality.

## Compiling .scss files

Store Front 2021 uses [SASS](https://sass-lang.com/) to build its CSS. `.scss` files are compiled into `app.css`, avoid modifying `app.css`. Otherwise, if for whatever reason you eventually do need to re-compile the `.scss` files, any changes to `app.css` would be lost. You're best off developing in you're own `.scss` file and adding it to the imports in `src/scss/app.scss`, which needs to be compiled to `src/css/app.css` using Gulp.

If you are compiling `.scss` files for the purpose of contributing to Store Front 2021, follow these steps:

_Note that steps 1 and 2 only need to be completed once per system, so no need to repeat them again._

1. Install [node.js](https://nodejs.org/),
2. CD into your local folder of Skeletal and run the `npm ci` command to install all relevant dependencies,
3. Run either of these two commands:
    - `npm run build` ??? this will compile your `.scss` files.
    - `npm run watch` ??? this will watch your `.scss` files and compile them as they change.

## Testing

We have a simple testing guide located [here](/testing.md).

## Contribute

<img src="https://design.neto.com.au/assets/uploads/howtogit01.jpg" width="500">

### Clone latest version of Store Front 2021

You want to download the latest version of Skeletal so your local version is up to date with the remote:

`git clone https://github.com/NetoECommerce/Skeletal.git`

If you already have a local version of Skeletal then you just need to update it to match the remote:

`git pull`

### Make a new branch

You do not want your changes to be on master, changes need to be reviewed to ensure it meets Neto standards and you could possible have made mistakes. You make a branch off the master branch so you have all the latest commits and can safely make  changes without affecting live code.

`git checkout -b "BRANCH-NAME"`

#### Naming branch

Branching name should be prefixed with how the pull request is helping Skeletal. Is this pull request fixing a bug?

`git checkout -b "hotfix/branch-title"`

Is this pull request adding a new feature or enhancement?

`git checkout -b "feature/branch-title"`

### Make changes and comment

Try to ensure your commit messages are frequent and descriptive. A commit should encompass one change, e.g redesigning home page and adding new pricing logic for product page would be two different commits. the home page redesign might have multiple template changes but it doesn't have anything to do with the pricing logic change on the product page.

`git add -A`

`git commit -m "commit message"`

#### Submit a pull request

When your branch is completed and ready for review you can submit a pull request. If you haven't already, push your branch up to the remote:

`git push`

You might need to set you the branch to be tracked as it is a new branch you made locally:

`git push -u origin "BRANCH-NAME"`

A pull request will need a description on what it is trying to achieve with this change and if possible, steps on how to view changes on a Neto site. This is neccessary as someone else will be reviewing your pull request and can't be expected to understand what it is doing/fixing just by reviewing the code.

## Review a pull request

<img src="https://design.neto.com.au/assets/uploads/howtogit02.jpg" width="500">

### Read pull request description

The person making the pull request will have left a description on what it is trying to achieve and how to reproduce it yourself.

This might be as simple as a style change and listing out where you can view this, or it might be some template/logic changes which require a few steps to reproduce. If it is unclear how to view the pull requests changes, please get in contact with the person that made the pull request.

### Test out code on dev site and do a code review

You should be able to view a working example of the changes on your Neto dev site based on the pull request description.

Ensure you have the most up to date version of the Skeletal master repo, then switch to the pull requests branch:

`git checkout "PULL-REQUEST-BRANCH"`

Then ensure you have the most up to date commits:

`git pull`

**Please Note:** This is one of the reasons users should do a branch instead of a fork. When you fork a repo, it makes a copy of the repo but under your users account, e.g If I forked Skeletal it work be in my repos instead of NetoECommerce. This makes it difficult to review as it no longer can be checked out while in the NetoECommerce/Skeletal repo.

#### Review a fork instead of branch

Open up the??`.git/config??file` and add a new line under??`[remote "origin"]`:

```
fetch = +refs/pull/*/head:refs/pull/origin/*
```

Now you can fetch and checkout any pull request so that you can test them:

```
# Fetch all pull request branches
git fetch origin

# Checkout out a given pull request branch based on its number
git checkout pull/origin/999
```

Keep in mind that these branches will be read only and you won't be able to push any changes. Branch name will be `pull/origin/PULL_REQUEST_NUMBER`.

When you have the pull request branch locally, push it into the theme directory to view the changes on your Neto dev site.

`/httpdocs/assets/themes/THEME-NAME`

`?nview=THEME-NAME`

### Comment on findings

After you have reviewed the pull request, add in your review:

- **Comment:** General feedback but not explicit approval
- **Approval:** Submit feedback and approve merging these changes into the master branch

If a pull requested is approval then an admin user will be notified and will be able to merge the branch into master.

- **Request feedback:** Submit feedback that must be addressed before the branch can be merged into master.

The person that submitted the pull request will be notified on your feedback and will address the issues before requesting the branch to be reviewed again.

## Support

The current version of Skeletal will only work on websites running Neto 6+. For older websites, you will need to install from a previous [release](https://github.com/NetoECommerce/Skeletal/releases/tag/2.4.0).

## Creators

Original Store Front theme Made w/ ???? by [Neto E-commerce Solutions](http://neto.com.au). Updated theme provided by [Online Retail Guy](https://www.onlineretailguy.com.au/)
