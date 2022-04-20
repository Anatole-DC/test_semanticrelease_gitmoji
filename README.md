<h1 align="center">TEST GITMOJI RELEASE</h1>

This repository is a test of semantic release with gitmoji.

A Django project was added to this repository to apply some new features, and commits, in order to test the pipeline, and the good behavior of the project.

___

**Technos :** Git, Gitmoji, Semantic Release

**Author :** [Anatole de Chauveron](https://github.com/Anatole-DC) _(Based on the work of [Nicolas Beaussart](https://github.com/beaussan/expr-gitmoji-releaserc))_

**Licence :** Free of use

___

## Summary

### Requirements

**NodeJS**

```bash
❯ node --version
v16.14.2
```

**Gitmoji**

```bash
❯ gitmoji --version
4.11.0
```

**Yarn**

```bash
❯ yarn --version
1.22.18
```

### Installation


**Install the dependencies**

You can start by creating a new project, with the techno of your choice.

In the repository, you are going to init a new yarn package, with the command :

```bash
❯ yarn init
```

Once you've given the asked informations, you can add the following dependencies to your project.

```bash
❯ yarn add semantic-release

❯ yarn add semantic-release-gitmoji
```

**Create a new Github Token**

Before we create the pipeline file for Github Actions, we are going to need a Github Token. To do that, go to your personal [developer settings](https://github.com/settings/tokens).

Create a new token by clicking on **Generate new token**. Check the `Worklow` radio button. It is required for your token to be able to push on your repositories.

> ⚠️ **Copy the token before exiting the page, you won't be able to access it once the page will be exited.**

Go to the Github page of your project and go to the section `settings/secrets/actions`, in which you will create a new repository secrets.

Call it `GH_TOKEN` (as `GITHUB_` is not allowed as a name), and paste the value of the token that you previously copied bellow.

**Workflow**

Finally you can add the workflow *.yml file to your project.

> Make sure that your your file is beeing placed in the `.github/workflows/` directory of your project.

You are now ready to use the project, and create your new release.

> ⚠️ If you changed the token name, or if your branch name is not `master`, make sure to apply those changes in the `release.yml` and `.releaserc.js` files.

### Usage

To start a new commit, add your modified files with a simple `git add <files>`.

Instead of running the usual `git commit -m "message"` command, we are going to run the following command :

```bash
❯ gitmoji -c
```

It will prompt you a message asking you to choose an emoji, according to your features (feature, bug fix, format...).

Enter your commit title, and eventually, your commit message.

Finnally, push your modifications on Github with the `git push` command.

**🎉 CONGRATULATIONS 🎉**

## Getting further

_For any questions about this repository, please contact the author at **adechauveron@gmail.com**._