# Release Cycle & Steps For Release

## Steps to be taken:

### 1. Prepare the Release

- Merge all relevant (feature/bug) PRs into the `develop` branch.

### 2. Create a Release Candidate
- Create a **Release Candidate PR** from `develop` to `staging` for review.
- Perform a thorough peer review of the PR to identify and resolve any bugs or issues.
- Conduct QA testing to ensure all changes are functional and meet requirements.
- Once approved by all reviewers and QA, merge the PR into the `staging` branch.

### 3. Finalize the Release
- Create a PR from `staging` to the `main` branch for final review.
- Ensure all changes are reviewed and approved by relevant stakeholders.
- Merge the PR into the `main` branch.

### 4. Update the `CHANGELOG.md`

- Compile a list of changes made in the release using the Git log:

```
git log v1.0.0..HEAD --pretty=format:"%h - %s" > 'release.note-project'

```
- Summarize the targets met and related commits from the `release.note-project` file.
- Update the `CHANGELOG.md` under the **Released** section at the top, following the existing convention.
- Move the changes to the new version section with the release version.

### 5. Create a Release Commit & Tag
- Create a release commit for the new version with ChangeLog:
  ```
  Release vX.X.XX
  ```
- Tag the release commit following the project convention (e.g., vX.X.X):
  ```
  git tag vX.X.X
  ```
- Push the release commit and tag:
  ```
  git push --tags
  git push
  ```

### 6. Backmerge Changes
- Backmerge the changes from `main` to `staging` using a fast-forward merge:
```
git checkout staging
git merge main --ff-only
git push
```
- Backmerge the changes from staging to develop using a fast-forward merge:
```
git checkout develop
git merge staging --ff-only
git push
```
### 7. Finalize the Release Process
- Verify that changes are synced across `main`, `staging`, and `develop` branches.
- Create a release under **Deployments** > **Releases** in the project.
