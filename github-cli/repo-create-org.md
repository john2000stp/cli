# Creating GitHub Repositories in Organizations with gh CLI

To create a remote repository on GitHub specifying an organization using the `gh` CLI:

## Basic Syntax

```bash
gh repo create ORGANIZATION/REPOSITORY-NAME --public
```

## Examples

Create a public repository in an organization:
```bash
gh repo create myorg/my-new-repo --public --description "My new repository"
```

Create and clone locally:
```bash
gh repo create myorg/my-new-repo --public --clone
```

Create a private repository:
```bash
gh repo create myorg/my-new-repo --private --description "Private project"
```

## Common Options

- `--public` - Make the repository public
- `--private` - Make the repository private
- `--internal` - Make the repository internal (for enterprise)
- `--clone` - Clone the new repository to current directory
- `--description "text"` - Add a description
- `--add-readme` - Add a README file
- `--gitignore template` - Add gitignore template
- `--license name` - Add open source license
- `--team name` - Grant access to organization team

## Requirements

- You need appropriate permissions in the organization to create repositories
- Must be authenticated with `gh auth login`

## Interactive Mode

For interactive creation:
```bash
gh repo create
```

This will prompt you for organization, name, visibility, and other options.