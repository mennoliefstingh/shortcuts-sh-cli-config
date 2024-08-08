# shortcuts-sh-cli-config
Template for a ~/.cli dir to collect, customize and configure your cli tooling

# Setup
- Fork this repository
- Clone it in your home dir and rename it to `.cli`
  - `cd ~`
  - `git clone git@github.com:[YOURNAME]/shortcuts-sh-cli-config.git`
  - `mv shortcuts-sh-cli-config .cli`
- Add the following to your `~/.zshrc`, `~/.bashrc` or equivalent:
```bash
# Export CLI setup
export PATH="$HOME/.cli/scripts:$PATH"

# Load alias collections from .cli/aliases
for file in /Users/menno/.cli/aliases/*.sh; do
    if [ -f "$file" ]; then
        source "$file"
    else
        echo "No .sh files found in /Users/menno/.cli/aliases/"
    fi
done
```
- Reload (`source ~/.zshrc`, `source ~/.bashrc` or restart your terminal)
