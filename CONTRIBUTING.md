# Eclipse Development Process Community Contributing Guide

This directory contains the source for the [Eclipse Development Process](eclipse_development_process.adoc) in AsciiDoc format, the build script, and generated output.
The build script is configured to generate output for a specific version of the document and running the build (`npm run build`) may overwrite any existing document.

The output files (eg., `*.html`) may be live documents that may be included by other documents found in the repository and also externally, so take care with what you commit.

## Installing NPM

NPM is required for generating the output files. 
Please have a look at [Get npm!](https://www.npmjs.com/get-npm)

## Installing Asciidoctor

Please allow NPM to install all dependencies by running `npm install`.

## AsciiDoc Syntax

Please refere to  [AsciiDoc Syntax Quick Reference](http://asciidoctor.org/docs/asciidoc-syntax-quick-reference/).

## Making changes

Follow [AsciiDoc Recommended Practices](https://asciidoctor.org/docs/asciidoc-recommended-practices/) when making changes.
In particular, the one sentence per line recommendation is important to us.
This makes it much easier to view the diffs in git.

As a sanity check, `npm test` should be run before committing.
It should be run automatically because npm install should setup Git a pre-coomit hook automatically.

Sometimes, it isn’t possible to fix all lint issue, e.g., because you’d like to try out something for testing or discussion.
In that case, you can use `git commit --no-verify` to temporarily bypass the check.

## Update Process

Please submit pull requests for any changes.
We’ll use pull requests for discussing them.

New requirements, ideas and significant changed should be captured in issues.
Larger items should be brought to the Architecture Council mailing list for discussion.
Discussion summary/results must be documented (and referenced) in pull requests and issues.

**No pull request** can be merged **without being reviewed**.

### Sign-off Process

All commits to code in the Eclipse organization **MUST** be signed off. This is done when committing from git passing the extra argument `-s` e.g.:

```shell
git commit -s -m "Improve the EDP"
```

For more info on contributing via Git, see [here](http://wiki.eclipse.org/Development_Resources/Contributing_via_Git).

### Small Changes

Changes less than 10 lines or so (e.g.: correcting typos, small changes to `README.adoc` and such-like) can be made directly on a branch.

Any change to `eclipse_development_process.adoc` and its related documents is **NEVER** considered a simple change. It requires a pull request and full EMO review and approval before merge.

## Branching Model

This repository uses two branches: `master` and `develop`.

`master` is the reviewed and approved *"current"* version of the Eclipse Development Process documents.

`develop` contains changes that are in progress (*"under development"*) and may not be *ready for production*, this is reviewed and approved by EMO and the Eclipse Foundation Board of Directors.

From the `develop` branch, you create *topic* branches to work on individual features and fixes. Once your feature/fix is ready to go, you request a merge into `develop` by opening a pull request.

Once develop is in a ready *"to be released"* state, we’ll create tag and a pull request to `master`. The pull request will be merged once all necessary reviews and approvals are in.
