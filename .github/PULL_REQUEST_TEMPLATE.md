# Pull Request template

Please, go through these steps before you submit a PR.

1. Make sure that:
   1. You have done your changes in a separate branch. Branches MUST have descriptive names that start with either the `fix/` or `feature/` prefixes. Good examples are: `fix/signin-issue` or `feature/issue-templates`.
   2. You have a descriptive commit message with a short title (first line).
   3. `npm test` doesn't throw any error. If it does, fix them first and amend your commit (`git commit --amend`).
   4. All your commits are signed (`git commit -s`).
   5. There are no merge commits in your branch (use Git Rebase instead).

2. After these steps, you're ready to open a pull request.
   1. Your pull request MUST NOT target the `master` branch on this repository. You probably want to target `develop` instead.
   2. Give a descriptive title to your PR, reference any existing issues and discussions.
   3. Provide a description of your changes.
   4. Put `closes #XXXX` in your comment to auto-close the issue that your PR fixes (if such).

IMPORTANT: Please review the [CONTRIBUTING.md](../CONTRIBUTING.md) file for detailed contributing guidelines.

## PLEASE REMOVE THIS TEMPLATE BEFORE SUBMITTING

#### Problem Description
* Describe the problem this PR is addressing.
* Reference any existing issues.

#### Proposed Changes
* Please summarize the proposed changes here

#### Benefits
* What are the gains by incorporatin the changes?

#### Challenges
* What are the drawbacks of the proposed changes?
* Are there any other consequences/implications?

#### References
* Add links to existing discussions, issues, etc.
