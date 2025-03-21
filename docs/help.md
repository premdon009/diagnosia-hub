# Help related to project.

## 1. Deno install problem in gitpod before project.

i tried to install deno in a single line command with 'curl -fsSL https://deno.land/install.sh | sh ' but after installing it is asking 'Edit shell configs to add deno to the PATH? (Y/n)' and also it tell to select bash, zsh and fish.

### Install Deno Without User Interaction

You can install Deno non-interactively and ensure it is added to your `PATH` automatically by running the following command:

```sh
curl -fsSL https://deno.land/install.sh | sh -s -- -f
```

#### Explanation

- `curl -fsSL https://deno.land/install.sh` → Downloads the install script.
- `| sh -s -- -f` → Passes the `-f` (force) flag to the script, which ensures automatic shell configuration without prompting.

#### What This Does

- Installs Deno to `~/.deno/bin`
- Modifies your shell profile (`.bashrc`, `.zshrc`, or `.config/fish/config.fish`) to add Deno to `PATH`

#### Applying Changes

After installation, **restart your terminal** or run:

```sh
export PATH="$HOME/.deno/bin:$PATH"
```

to apply the changes immediately.
