# Pull Request Process

Most of projects utilize the PR mechanisms from services like Github, Gitlab and Bitbucket.

## Pre-PR Checklist

Before creating the pull request, make sure to do the following:

1. Review your own code. Ideally, you're doing this with each commit that you make in addition to a final look when previewing the PR.
2. Integrate the latest changes by merging develop into your feature/* branch.
3. Make sure to address any outstanding TODOs or commented out code that you intended to clean up.
4. Make sure there are no new compilation warnings or errors. Don't break the build!
5. Make sure all of the unit tests pass.

## Creating the PR

1. Author creates a PR from their feature/* branch into develop. Most of the time the default title and review description based on commit messages should be sufficient, but any additional context is welcome.
2. The repository should be configured to automatically add default reviewers to each PR, but if there is anyone missing, the author should make sure to add them manually.
3. The repository should have a [pull request template](../.github/pull-request-template.md) and follow instructions provided in the template.
4. If not previewed during the PR creation process, the author should immediately perform a self-review after the PR is created to spot and fix any final details before others start reviewing.

## PR Feedback Process

1. Reviewers review the code, adding comments and suggestions for improvements.
2. The author implements the suggested feedback or starts a discussion in order to get clarification or provide an alternate opinion.
3. Once satisfied with the implemented improvements (if any), the reviewer "approves" the PR.

## Merging the PR

1. Once all required reviewers have approved the PR, the author merges the PR.
2. Once merged, the feature/* branch can be removed.
3. After merging, the author should build and run the app to verify functionality one last time. This is especially important if there were merge conflicts that had to be resolved before the merge.
4. After merging, the author is also responsible for updating the relevant ticket(s) in the sprint board as well.
