# Contributing content to Angular Study Guide

As a contributor, here are the guidelines we would like you to follow:

 - [Question or Problem?](#question)
 - [Issues and Bugs](#issue)
 - [Content Requests](#content)
 - [Submission Guidelines](#submit)
 - [Coding Rules](#rules)
 - [Commit Message Guidelines](#commit)


## <a name="question"></a> Got a Question or Problem?

Do not open issues for general support questions as we want to keep GitHub issues for bug reports and content requests.
Instead, we recommend using our channel at [Angular Nation][nation] to ask support-related questions.


## <a name="issue"></a> Found a Bug?

If you find a bug in the source code, you can [submit an issue](#submit-issue) to our [GitHub Repository][github].
Even better, you can [submit a Pull Request](#submit-pr) with a fix.


## <a name="content"></a> Missing a Content?
You can *request* a new content by [submitting an issue](#submit-issue) to our GitHub Repository.
If you would like to *add* new content, please first open an issue and outline your proposal so that it can be discussed. This process allows us to better coordinate our efforts, prevent duplication of work, and help you to craft the change.


## <a name="submit"></a> Submission Guidelines


### <a name="submit-issue"></a> Submitting an Issue

Before you submit an issue, please search the issue tracker, maybe an issue for your problem already exists and the discussion might inform you of workarounds readily available.

Before fixing a bug we need to reproduce and confirm it. Consider providing a minimal reproduction along with reporting the issue.
Having a minimal reproducible scenario gives us a wealth of important information without going back and forth with additional questions.

A minimal reproduction allows us to quickly confirm a bug (or point out a coding problem) as well as confirm that we are fixing the right problem.

You can file new issues at our [GitHub Repository](https://github.com/Angular-community-collab/angular-study-guide).


### <a name="submit-pr"></a> Submitting a Pull Request (PR)

Before you submit your Pull Request (PR) consider the following guidelines:

1. Search [GitHub](https://github.com/Angular-community-collab/angular-study-guide/pulls) for an open or closed PR that relates to your submission.
   You don't want to duplicate existing efforts.

2. Clone the Angular-community-collab/angular-study-guide repo.

3. In your cloned repository, make your changes in a new git branch:

     ```shell
     git checkout -b my-fix-branch master
     ```

4. Create your patch, **including appropriate test cases (TBD)**.

5. Follow our [Coding Rules](#rules).

6. Run the full test suite and ensure that all tests pass (TBD).

7. Commit your changes using a descriptive commit message that follows our [commit message conventions](#commit).

     ```shell
     git commit --all
     ```

8. Push your branch to GitHub:

    ```shell
    git push -u origin my-fix-branch
    ```

9. In GitHub, send a pull request to `angular-study-guide:master`.

### Reviewing a Pull Request

If we ask for changes via code reviews then:

1. Make the required updates to the code.

2. Create a fixup commit and push to your branch (this will update your Pull Request):

    ```shell
    git commit --all --fixup HEAD
    git push
    ```
    For more info on working with fixup commits see the [Angular fixup commit guide](https://github.com/angular/angular/blob/master/docs/FIXUP_COMMITS.md).

That's it! You are done!


## <a name="rules"></a> Coding Rules
To ensure consistency throughout the source code, keep these rules in mind as you are working:

* All content or bug fixes **must be tested** by one or more specs (unit-tests) (TBD).
* We follow the official [Angular Style Guide][style-guide].


## <a name="commit"></a> Commit Message Format

*This specification is inspired by and supersedes the [Angular commit message format][commit-message-format].*

We have very precise rules over how our Git commit messages must be formatted.
This format leads to **easier to read commit history**.

Each commit message consists of a **header**, a **body**, and a **footer**.


```
<header>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

The `header` is mandatory and must conform to the [Commit Message Header](#commit-header) format.

The `body` is not mandatory.
When the body is present it must conform to the [Commit Message Body](#commit-body) format.

The `footer` is optional. The [Commit Message Footer](#commit-footer) format describes what the footer is used for and the structure it must have.


#### <a name="commit-header"></a>Commit Message Header

```
<type>(<scope>): <short summary>
  │       │             │
  │       │             └─⫸ Summary in present tense. Not capitalized. No period at the end.
  │       │
  │       └─⫸ Commit Scope: (TBD)
  │                          
  │                          
  │
  └─⫸ Commit Type: docs|feat|fix|style|refactor|(test?)
```

The `<type>` and `<summary>` fields are mandatory, the `(<scope>)` field is optional.


##### Type

Must be one of the following:

* **docs**: Documentation only changes
* **feat**: A new content
* **fix**: A bug fix
* **style**: A code change that applies the style guide
* **refactor**: A code change that neither fixes a bug nor adds a content
* **test**: Adding missing tests or correcting existing tests (TBD)


##### Scope
The scope should be the name of the Angular Study topic affected.

The following is the list of supported scopes:

* `TBD`

There are currently a few exceptions to the "use topic name" rule:

* none/empty string: useful for `test` and `refactor` changes that are done across all content (e.g. `test: add missing unit tests`).


##### Summary

Use the summary field to provide a succinct description of the change:

* use the imperative, present tense: "change" not "changed" nor "changes"
* don't capitalize the first letter
* no dot (.) at the end


#### <a name="commit-body"></a>Commit Message Body

Just as in the summary, use the imperative, present tense: "fix" not "fixed" nor "fixes".

Explain the motivation for the change in the commit message body. This commit message should explain _why_ you are making the change.
You can include a comparison of the previous behavior with the new behavior in order to illustrate the impact of the change.


#### <a name="commit-footer"></a>Commit Message Footer

The footer is the place to reference GitHub issues, and other PRs that this commit closes or is related to.

```
Fixes #<issue number>
```




[commit-message-format]: https://github.com/angular/angular/blob/master/CONTRIBUTING.md#-commit-message-format
[github]: https://github.com/Angular-community-collab/angular-study-guide
[style-guide]: https://angular.io/guide/styleguide
[nation]: https://www.angularnation.net/groups/4044265