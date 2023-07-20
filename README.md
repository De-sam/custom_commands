# Custom Git Commands

This repository contains three custom Git commands to streamline your Git workflow. To use these commands, follow the instructions below.

## Installation

To get started, follow these steps:

1. Clone the repository:

```bash
git clone https://github.com/De-sam/custom_commands.git
```

2. Navigate to the cloned directory:

```bash
cd custom_commands
```

3. Make the scripts executable:

```bash
chmod +x clone gitpush git_push
```

4. Include the repository in your PATH:

To make the commands available globally in your home directory, add the following line to your `~/.bashrc` file:

```bash
export PATH="$PATH:$HOME/custom_commands"
```

Save the file, and then apply the changes by running:

```bash
source ~/.bashrc
```

Now, you can use the custom commands from any directory.

## Command Descriptions

### 1. `clone`

This command allows you to clone a GitHub repository securely by providing your GitHub Personal Access Token and github username. If you have already set up these parameters, it will be read from the file "~/.github_access_token_github_username." If the file does not exist, the command will prompt you to enter the token and username.

Usage:

```bash
clone <repository_name>
```

Example:

```bash
clone example_repo
```

### 2. `gitpush`

This command automates the process of adding all changes, committing them with a custom message, and pushing them to the remote repository. You can use this command within a subdirectory present in a GitHub repository directory. This way, you can make changes in the subdirectory, add, commit, and push all changes in one go, and then navigate back to the subdirectory.

Usage:

```bash
gitpush <commit_message>
```

Example:

```bash
cd path/to/subdirectory
# Make changes to files in the subdirectory
gitpush "Fix: Updated the documentation."
cd -
```

### 3. `git_push`

The `git_push` command is intended to be used directly in the parent GitHub repository directory. It simplifies the process of adding all changes, committing them with a custom message, and pushing them to the remote repository.

Usage:

```bash
git_push <commit_message>
```

Example:

```bash
# Make changes to files in the parent repository directory
git_push "Feature: Added new feature."
```

## Note

Before using the custom commands, ensure that you have Git installed and set up on your system. Additionally, make sure you have the necessary permissions to clone, add, commit, and push to the repositories.

For any issues or suggestions related to the custom commands, please open an issue on the [GitHub repository](https://github.com/De-sam/custom_commands). We welcome your feedback and contributions!

