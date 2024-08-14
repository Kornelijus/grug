# grug

**G**rep **R**ecursive **U**tility for **G**it

Simple script to search through the main branches of all of your git repositories locally using `git grep`.  
It will periodically run `git fetch` before searching to ensure results are (kinda) up to date.

Shout out to everyone who can't afford GitLab Enterprise Edition :skull:

# Installation

```sh
# Clone and navigate to the repo
git clone https://github.com/Kornelijus/grug.git
cd grug

# Add current dir with script to your PATH
# bash
echo "export PATH=\$PATH:$(pwd)" > ~/.bashrc

# zsh
echo "export PATH=\$PATH:$(pwd)" > ~/.zshrc
```

# Configuration

| Environment Variable       | Description                                                | Default Value     |
| -------------------------- | ---------------------------------------------------------- | ----------------- |
| `GRUG_ROOT`                | Path to directory where your git repositories are located. | Current directory |
| `GRUG_DEFAULT_BRANCH`      | Default branch to search through.                          | `master`          |
| `GRUG_FETCH_INTERVAL_MINS` | How often `git fetch` should be run on the main branches.  | `60`              |
