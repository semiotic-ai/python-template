# Contributing

The following enumerates best practices for contributing and collaborating on Semiotic Labs repositories.
Much credit is given to the variety of sources from which we pull, including [ColPrac](https://github.com/SciML/ColPrac).

## PRs Versus Committing to `main`

If you are one of the main developers (collaborators) on a repository, you should probably default to committing to `main`.
If you are new to this repository, or are not considered a collaborator, you should instead contribute via PRs.

**NOTE:** Collaborators may also contribute via PRs if they'd like to.
However, we ask that in such cases, collaborators ensure PRs are small efforts that require less than a day.
This is because we want to minimise merge conflicts due to branches diverging.
Collaborators may merge their own PRs.

### Becoming a Collaborator

To become a collaborator, you should have approval from an existing collaborator.
Typically, our goal is to ensure that everyone is a collaborator, as the less time we spend reviewing PRs, the faster we move.
Feel free to ask to become a collaborator whenever.
We will determine whether to give you collaborator access based on:

- Well-written, useful tests
- Code testability
- Code style
- Documentation
- Following the best practices for commits and PRs.
- Constructive engagement in issues.

## Commits

Commits must follow the following rules.

1. Commits should match the existing code style.
2. If you add new a function, class, or type, or if you fix a bug, you must document and test it.
Use your best judgement to determine what type of tests make the most sense for your addition.
For example, you could write unit tests, acceptance tests, or both.
3. Each commit should only do one thing.
For example, if you refactor, don't also add a new feature or a bugfix.
A good rule of thumb is that if it is difficult to come up with a concise, descriptive commit message per [Conventional Commits](https://kapeli.com/cheat_sheets/Conventional_Commits.docset/Contents/Resources/Documents/index), your commit is probably doing too much.
4. Commits must pass unit tests, static analysis, and code formatting.
Ideally, you should also run them against acceptance tests.
5. The commit message must follow practices from [Conventional Commits](https://kapeli.com/cheat_sheets/Conventional_Commits.docset/Contents/Resources/Documents/index).
A key rule of conventional commits that people often forget is that the subject should be in the imperative mood.
For example, `feat: adding a CSV writer` is incorrect.
You would use `feat: add a CSV writer`.
One way to think about it is using the phrase `This commit will <subject>`.
For our previous example, `This commit will add a CSV writer`.
Tools such as [Emacs magit](https://magit.vc/), [fugitive.vim](https://github.com/tpope/vim-fugitive) and [VSCode Source Control](https://code.visualstudio.com/docs/sourcecontrol/overview) have nice interfaces for staging chunks within files.
These can help you in following this rule.

## PRs

PRs consist of commits and should follow the above rules.

Furthermore,

1. PRs must have at least one approval from a collaborator before someone merges them.
2. PRs should pass at least the commit and acceptance stages of the release pipeline before merging.
3. PRs should only do one thing and should be small.
Ideally, each PR should take less than a day so that the branches don't diverge too severely.
4. PRs must be associated with issues.
