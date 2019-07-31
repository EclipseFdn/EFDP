# Eclipse Development Process Community Contributing Guide

This directory contains the source for the [Eclipse Development Process](eclipse_development_process.adoc) in AsciiDoc format, the build script, and generated output.

## Update Process

Please submit pull requests for any changes. We’ll use pull requests for discussing them.

New requirements, ideas and significant changed should be captured in issues. Discussion summary/results must be documented (and referenced) in pull requests and issues.

**No pull request** can be merged **without being reviewed**.

### Eclipse Contributor Agreement

Before your contribution can be accepted by the project team contributors must
electronically sign the Eclipse Contributor Agreement (ECA).

* http://www.eclipse.org/legal/ECA.php

Commits that are provided by non-committers must have a Signed-off-by field in
the footer indicating that the author is aware of the terms by which the
contribution has been provided to the project. The non-committer must
additionally have an Eclipse Foundation account and must have a signed Eclipse
Contributor Agreement (ECA) on file.

For more information, please see the Eclipse Committer Handbook:
https://www.eclipse.org/projects/handbook/#resources-commit

### Sign-off Process

All commits to code in the Eclipse organization **must** be signed off. 
This is done when committing from Git passing the extra argument `-s` e.g.:

```shell
git commit -s -m "Improve the EDP"
```

For more info on contributing via Git, see [the Eclipse Foundation Wiki](http://wiki.eclipse.org/Development_Resources/Contributing_via_Git).

### Small Changes

Changes less than 10 lines or so (e.g.: correcting typos, small changes to `README.adoc` and such-like) can be made directly on a branch.

Any change to `eclipse_development_process.adoc` and its related documents is **never** considered a simple change. 
It requires a pull request and full EMO review and approval before merge.

## Branching Model

This repository uses two branches: `master` and `develop`.

`master` is the *reviewed and approved* **current** version of the Eclipse Development Process documents.

`develop` contains changes that are in progress (*"under development"*) and may not be *ready for production*, this is changes not reviewed and approved by EMO and the Eclipse Foundation Board of Directors.

From the `develop` branch, you create *topic* branches to work on individual features and fixes. Once your feature/fix is ready to go, you request a merge into `develop` by opening a pull request.

Once develop is in a ready *"to be released"* state, we’ll create a tag and a pull request to `master`. The pull request will be merged once all necessary reviews and approvals are in.
