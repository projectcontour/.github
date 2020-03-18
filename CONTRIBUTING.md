# Contributing

Thanks for taking the time to join our community and start contributing.
These guidelines will help you get started with the Contour project.
Please note that we require [DCO sign off](#dco-sign-off).

## Contribution workflow

This section describes the process for contributing a bug fix or new feature.

### Before you submit a pull request

This project operates according to the _talk, then code_ rule.
If you plan to submit a pull request for anything more than a typo or obvious bug fix, first you _should_ raise an issue to discuss your proposal, before submitting any code.

Depending on the size of the feature you may be expected to first write a design proposal.

### Commit message and PR guidelines

- Have a short subject on the first line and a body. The body can be empty.
- Use the imperative mood (ie "If applied, this commit will (subject)" should make sense).
- There must be a DCO line ("Signed-off-by: David Cheney <cheneyd@vmware.com>"), see [DCO Sign Off](#dco-sign-off) below
- Put a summary of the main area affected by the commit at the start,
with a colon as delimiter. For example 'docs:', 'internal/(packagename):', 'design:' or something similar.
- Try to keep your number of commits in a PR low. Generally we
tend to squash before opening the PR, then have PR feedback as
extra commits.
- Do not merge commits that don't relate to the affected issue (e.g. "Updating from PR comments", etc). Should
the need to cherrypick a commit or rollback arise, it should be clear what a specific commit's purpose is.
- If master has moved on, you'll need to rebase before we can merge,
so merging upstream master or rebasing from upstream before opening your
PR will probably save you some time.
- PRs *must* include a `Fixes #NNNN` or `Updates #NNNN` comment. Remember that
`Fixes` will close the associated issue, and `Updates` will link the PR to it.

#### Commit message template

```
<packagename>: <imperative mood short description>

Updates #NNNN
Fixes #MMMM

Signed-off-by: Your Name <you@youremail.com>

<longer change description/justification>

```

#### Sample commit message

```
internal\contour: Add quux functions

Fixes #xxyyz

Signed-off-by: Your Name <you@youremail.com>

To implement the quux functions from #xxyyz, we need to
florble the greep dots, then ensure that the florble is
warbed.
```

### Pre commit CI

Before a change is submitted it should pass all the pre commit CI jobs.
If there are unrelated test failures the change can be merged so long as a reference to an issue that tracks the test failures is provided.

## DCO Sign off

All authors to the project retain copyright to their work. However, to ensure
that they are only submitting work that they have rights to, we are requiring
everyone to acknowledge this by signing their work.

Any copyright notices in this repository should specify the authors as "The
project authors".

To sign your work, just add a line like this at the end of your commit message:

```
Signed-off-by: David Cheney <cheneyd@vmware.com>
```

This can easily be done with the `--signoff` option to `git commit`.

By doing this you state that you can certify the following (from https://developercertificate.org/):

```
Developer Certificate of Origin
Version 1.1

Copyright (C) 2004, 2006 The Linux Foundation and its contributors.
1 Letterman Drive
Suite D4700
San Francisco, CA, 94129

Everyone is permitted to copy and distribute verbatim copies of this
license document, but changing it is not allowed.

Developer's Certificate of Origin 1.1

By making a contribution to this project, I certify that:

(a) The contribution was created in whole or in part by me and I
    have the right to submit it under the open source license
    indicated in the file; or

(b) The contribution is based upon previous work that, to the best
    of my knowledge, is covered under an appropriate open source
    license and I have the right under that license to submit that
    work with modifications, whether created in whole or in part
    by me, under the same open source license (unless I am
    permitted to submit under a different license), as indicated
    in the file; or

(c) The contribution was provided directly to me by some other
    person who certified (a), (b) or (c) and I have not modified
    it.

(d) I understand and agree that this project and the contribution
    are public and that a record of the contribution (including all
    personal information I submit with it, including my sign-off) is
    maintained indefinitely and may be redistributed consistent with
    this project or the open source license(s) involved.
```
