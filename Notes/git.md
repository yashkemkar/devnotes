# Git Notes
## Introduction

### What makes a Good Commit vs Bad Commit
#### Atomic changes
Any time something is changed, it must be committed to Github, however there is a difference between a good commit and bad commit. A good commit should consist of only one atomic change in the code for example "added user authentication", whereas if you have multiple changes then that would be a bad commit - "added user authentication and update UI styles.

#### Descriptive Commit Message
Every commit message should describe exactly what was done, rather than a generalised description such as "fixed bug" - this does not help anyone who looks at the code. The message should be specific and descriptive such as "Fix correct null pointer exception in user login.
```
# Good commit
git commit - m "Add user authentication"
### .gitignore
We can use a .gitignore file in our project to include any files that we don't want to be uploaded to github. The way this is done is by stating the file extensions within the code.

For example, we could exclude .env files which store special API keys with are used to authenticate you with the API. These keys must be protected.