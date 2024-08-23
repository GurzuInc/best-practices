 # Commits
 ## Intro
Commit early, commit often! Try to remember to push any pending commits to the remote repo at the end of every day so that all in-progress work is backed up.
Commit messages should be detailed and helpful - avoid anything that's not a complete sentence. You should aim to tell a story in the commit message (i.e. what was broken and how it was fixed). A good rule of thumb to follow is to begin commit messages with a verb.

The commit message should be structured as follows:
```
    <type>[optional scope]: <description>
    [optional body]
    [optional footer]
```

## Getting Started
For easier implementation of following above convention for commit message, we'll create a template on our development machine and use it to structured our commit messages. Follow following steps to create and getting started with commit template,

- First, create a .txt file in a directory of your choice that will act as the template.
```touch commit-conventions.txt```
- Open the .txt file with the editor of your choice. Git will ignore lines that begin with a # or ; by default, so we’ll use those to make a template of ignored lines that only you will see when you’re making commits.
```
# ----------------------------------------------------------
# Header - type(scope): Brief description
# ----------------------------------------------------------
# * feat            A new feature - SemVar PATCH
# * fix             A bug fix - SemVar MINOR
# * BREAKING CHANGE Breaking API change - SemVar MAJOR
# * docs            Change to documentation only
# * style           Change to style (whitespace, etc.)
# * refactor        Change not related to a bug or feat
# * perf            Change that affects performance
# * test            Change that adds/modifies tests
# * build           Change to build system
# * ci              Change to CI pipeline/workflow
# * chore           General tooling/config/min refactor
# ----------------------------------------------------------



# ----------------------------------------------------------
# Body - More description, if necessary
# ----------------------------------------------------------
# * Motivation behind changes, more detail into how
# functionality might be affected, etc.
# ----------------------------------------------------------


# ----------------------------------------------------------
# Footer - Associated issues, PRs, etc.
# ----------------------------------------------------------
# * Ex: Resolves Issue #207, see PR #15, etc.
# ----------------------------------------------------------
```


- To add the template to your global git config, enter the following command on terminal,
```git config --global commit.template path/to/your/commit-conventions.txt```
- Now whenever you’re making a commit, instead of the typical ```git commit -m "A brief commit message"``` , just enter ```git commit``` to open your default editor with the template in place. You’ll automatically have a guide to choose conventions to create a structured message.
For example,
```
# ----------------------------------------------------------
# Header - type(scope): Brief description
# ----------------------------------------------------------
# * feat            A new feature - SemVar PATCH
# * fix             A bug fix - SemVar MINOR
# * BREAKING CHANGE Breaking API change - SemVar MAJOR
# * docs            Change to documentation only
# * style           Change to style (whitespace, etc.)
# * refactor        Change not related to a bug or feat
# * perf            Change that affects performance
# * test            Change that adds/modifies tests
# * build           Change to build system
# * ci              Change to CI pipeline/workflow
# * chore           General tooling/config/min refactor
# ----------------------------------------------------------
docs: Update README with contributing instructions

# ----------------------------------------------------------
# Body - More description, if necessary
# ----------------------------------------------------------
# * Motivation behind changes, more detail into how
# functionality might be affected, etc.
# ----------------------------------------------------------
Adds a CONTRIBUTING.md with PR best practices, code style
guide, and code of conduct for contributors.
# ----------------------------------------------------------
# Footer - Associated issues, PRs, etc.
# ----------------------------------------------------------
# * Ex: Resolves Issue #207, see PR #15, etc.
# ----------------------------------------------------------
Closes #9
```

- Make sure description does not exceed 60 characters to ensure readability (the commented lines are 60 characters long and act as guides for when to use a line break). The “body” optionally elaborates on the changes made, and the “footer” optionally notes any issue/PR the commit is related to.
- Final commit message will simply look as follows,
```
docs: Update README with contributing instructions
   
Adds a CONTRIBUTING.md with PR best practices, code style
guide, and code of conduct for contributors.

Closes #9
```
  
## Miscellaneous
If you use Vim or Neovim, and you want to speed up the process even more, you can add this to your git config:
```
# Neovim
git config --global core.editor=nvim +16 -c 'startinsert'

# If above command fails
git config --global core.editor "nvim +16 +startinsert"

# Vim
git config --global core.editor "vim +16 +startinsert"
```

This sets the default editor to Neovim (or Vim), and places the cursor on line 16 in Insert Mode as soon the editor opens.

Further, if you don't want your template to have following text,

```
# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit. #
# On branch develop
# Your branch is up to date with 'origin/develop'. #
# Changes to be committed:
# modified: App.js
#
```
just run following command,
```
git config --global commit.status false
```
 