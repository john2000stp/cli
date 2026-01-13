# Creating a GitHub Repository with GitHub CLI

## Command
```bash
gh repo create <repo-name> --private --source=. --remote=origin --push
```

## What this command does:
- `gh repo create <repo-name>` - Creates a new repository with the specified name
- `--private` - Makes the repository private
- `--source=.` - Uses the current directory as the source
- `--remote=origin` - Adds the GitHub repository as the 'origin' remote
- `--push` - Pushes the current branch to the remote repository

## Example:
```bash
gh repo create neptune --private --source=. --remote=origin --push
```

## Result:
- ✓ Creates private repository on GitHub
- ✓ Adds remote origin
- ✓ Pushes existing commits
- ✓ Sets up branch tracking

## Prerequisites:
- GitHub CLI (`gh`) must be installed and authenticated
- Must be in a git repository directory
- Must have commits to push