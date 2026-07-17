# Contributing to SmartResume

First off, thank you for considering contributing to SmartResume! It's people like you that make SmartResume such a great tool.

## Where do I go from here?

If you've noticed a bug or have a feature request, make sure to check our [Issues](https://github.com/Vivek9544/SmartResume/issues) first to see if it's already being worked on. If not, feel free to open a new issue using our templates!

## Fork & create a branch

If this is something you think you can fix, then fork SmartResume and create a branch with a descriptive name.

A good branch name would be (where issue #325 is the ticket you're working on):

```sh
git checkout -b 325-add-new-template
```

## Get the test suite running

Make sure you have followed the Installation instructions in the `README.md`. 
Ensure your local environment is running correctly before starting your development.

## Implement your fix or feature

At this point, you're ready to make your changes! Feel free to ask for help; everyone is a beginner at first.

## Code Style

- Use ESLint to lint your code before committing.
- Ensure your code follows the existing style and architecture.
- Keep components small and reusable.
- Use Tailwind CSS utility classes for styling where possible.

## Make a Pull Request

At this point, you should switch back to your master branch and make sure it's up to date with SmartResume's master branch:

```sh
git remote add upstream git@github.com:Vivek9544/SmartResume.git
git checkout master
git pull upstream master
```

Then update your feature branch from your local copy of master, and push it!

```sh
git checkout 325-add-new-template
git rebase master
git push --set-upstream origin 325-add-new-template
```

Finally, go to GitHub and make a Pull Request! We use a Pull Request template, please make sure to fill it out as completely as possible.

## Keeping your Pull Request updated

If a maintainer asks you to "rebase" your PR, they're saying that a lot of code has changed, and that you need to update your branch so it's easier to merge.

Thank you for contributing!
