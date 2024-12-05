# Git Extensions

A collection of useful Git extensions to enhance your Git workflow. These scripts provide additional functionality to Git through custom commands.

## Extensions

- **git-checkout**: Interactive branch checkout using fuzzy search. Uses `fzf` to provide a searchable list of all branches (local and remote) for easy checkout.
- **git-clean-branches**: Interactive tool to safely clean up local branches that don't have tracking remotes. Uses `fzf` for a user-friendly selection interface.
- **git-clone-worktree**: Clone a repository with worktree support. Sets up a bare repository with a clean worktree structure for better branch management.
- **git-fixup**: Create and automatically rebase fixup commits, making it easier to modify previous commits.
- **git-force-push**: Safe force-push command that uses --force-with-lease and --force-if-includes to prevent accidental overwrites of others' work.
- **git-sync**: Synchronizes branches with remote repository. Can sync the default branch or a specified branch with a given remote.

## Installation

1. Clone this repository:

   ```bash
   git clone <repository-url> ~/gitExtensions
   ```

2. Make the scripts executable:

   ```bash
   chmod +x ~/gitExtensions/git-*
   ```

3. Add the directory to your PATH or create symbolic links to the scripts in a directory that's already in your PATH.

4. Add aliases to your `~/.gitconfig`:
   ```ini
   [alias]
       clean-branches = !~/gitExtensions/git-clean-branches
       fixup = !~/gitExtensions/git-fixup
       # ...
   ```

## Requirements

- Bash 4.x or higher
- Git 2.x or higher
- `fzf` (for git-clean-branches and git-co)

## Contributing

Feel free to submit issues, fork the repository, and create pull requests for any improvements.

## License

This project is open source and available under the MIT License.
