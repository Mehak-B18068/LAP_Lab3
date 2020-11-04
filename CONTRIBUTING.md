# HOW TO CONTRIBUTE

Getting started, building, and testing
--------------------------------------

If you haven't already, take a look at the project's
[README.md file](README.md)
and the [documentation](https://github.com/Ruchika06/LAP_Lab3/wiki),
and try adding type annotations to your file.

#### Code of Conduct

Everyone participating in this community, and in particular in our
issue tracker, pull requests, is expected to treat
other people with respect and more generally to follow the guidelines
articulated in the [Python Community Code of
Conduct](https://www.python.org/psf/codeofconduct/).


Submitting Changes
------------------

Even more excellent than a good bug report is a fix for a bug, or the
implementation of a much-needed new feature. (*)  We'd love to have
your contributions.

(*) If your new feature will be a lot of work, we recommend talking to
    us early -- see below.

We use the usual GitHub pull-request flow, which may be familiar to
you if you've contributed to other projects on GitHub.  For the mechanics,
[GitHub's own documentation](https://help.github.com/articles/using-pull-requests/).

## REQUIRED MEASURES

Core developers should follow these rules when processing pull requests:

* Always wait for tests to pass before merging PRs.
* Use "[Squash and merge](https://github.com/blog/2141-squash-your-commits)"
  to merge PRs.
* Delete branches for merged PRs (by core devs pushing to the main repo).
* Edit the final commit message before merging to conform to the following
  style (we wish to have a clean `git log` output):
  * When merging a multi-commit PR make sure that the commit message doesn't
    contain the local history from the committer and the review history from
    the PR. Edit the message to only describe the end state of the PR.
  * Make sure there is a *single* newline at the end of the commit message.
    This way there is a single empty line between commits in `git log`
    output.
  * Split lines as needed so that the maximum line length of the commit
    message is under 80 characters, including the subject line.
  * Capitalize the subject and each paragraph.
  * Make sure that the subject of the commit message has no trailing dot.
  * Use the imperative mood in the subject line (e.g. "Fix typo in README").
  * If the PR fixes an issue, make sure something like "Fixes #xxx." occurs
    in the body of the message (not in the subject).
  * Use Markdown for formatting.
  * For each important variable, add a single comment line in proper format
  * For each function, add a `multiline docstring` at the start of the body describing the use of the function, the parameters and the return value.
  * Update the `requirements.txt` in the correct format, in case you add a new dependency.
  
## Example functions following code style

```python
def func(a):
    """
    func(a) increments the value of a returns it.
    @params:
        a: int
    @return:
        int
    """
    a = a + 1
    return a
```


## Contributing code

1. Clone the repository.
2. Checkout a new branch : `git checkout -b <name>_<feature>`.
3. Make changes.
4. Stage only required files to commit : `git add <Files_Changed>`. Don't add files you did not intentionally changed.
5. Commit with a proper message `git commit -m "message"`.
6. Push the branch : `git push origin <name>_<feature>`. Remember NOT to push `main` branch.
7. Create a Pull Request.
8. After the PR is merged, delete the local branch : `git checkout main && git branch -D <name>_<feature>`.
9. Pull the latest main branch : `git pull`.
10. Repeat Steps 2 to 6 for further contributions.

NOTE: Don't delete the branch unless the PR is merged.

### Other labels

* **needs discussion**: This issue needs agreement on some kind of
  design before it makes sense to implement it, and it either doesn't
  yet have a design or doesn't yet have agreement on one.
* **feature**, **bug**, **crash**, **refactoring**, **documentation**:
  These classify the user-facing impact of the change.  Specifically
  "refactoring" means there should be no user-facing effect.
* **topic-** labels group issues touching a similar aspect of the
  project, for example PEP 484 compatibility, a specific command-line
  option or dependency.
