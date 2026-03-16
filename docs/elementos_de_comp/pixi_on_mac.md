Pixi Not Working on Mac

If the `pixi` command is not working on your Mac, the most common cause is that the `~/.pixi/bin` directory is not in your system's `PATH`. This often happens when Pixi is installed via Homebrew, which does not automatically update your `PATH`.

### Solution:
Update your shell configuration file to include `~/.pixi/bin` in the `PATH`:

- For **zsh** (default on macOS), edit `~/.zshrc`:
  ```zsh
  echo 'export PATH="$HOME/.pixi/bin:$PATH"' >> ~/.zshrc
  ```
- For **bash**, edit `~/.bashrc` or `~/.profile`:
  ```zsh
  echo 'export PATH="$HOME/.pixi/bin:$PATH"' >> ~/.bashrc
  ```

After making the change, reload your shell configuration:
```zsh
source ~/.zshrc  # for zsh
# or
source ~/.bashrc  # for bash
```

Alternatively, **reinstall Pixi using the official script** to ensure the `PATH` is set automatically:
```zsh
curl -fsSL https://pixi.sh/install.sh | zsh
```

This method updates your shell configuration and adds `~/.pixi/bin` to the `PATH` automatically.

> 💡 **Note**: If you're using a CI/CD environment (like GitHub Actions) and see the `pixi` command missing, it may be due to a recent change in the Mac OS runner image (e.g., `20240911.3`). In such cases, manually add `~/.pixi/bin` to the `PATH` in your workflow.