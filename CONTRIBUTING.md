```markdown
# Contributing to Rice Cooker (`rcr`)

Thank you for your interest in contributing to `rcr`! This project aims to simplify Arch Linux configuration scripting for ricing enthusiasts. We welcome contributions in the form of bug fixes, feature additions, documentation improvements, or feedback.

## How to Contribute

1. **Fork the Repository**:
   - Fork the project on GitHub: https://github.com/<your-username>/rcr
   - Clone your fork:
     ```bash
     git clone https://github.com/<your-username>/rcr.git
     ```

2. **Create a Branch**:
   - Create a new branch for your changes:
     ```bash
     git checkout -b feature/your-feature-name
     ```

3. **Make Changes**:
   - Follow the coding style in the existing `rcr` script (e.g., consistent Bash formatting, clear comments).
   - Test your changes thoroughly on an Arch Linux system.
   - Update documentation (e.g., `README.md`) if needed.

4. **Commit and Push**:
   - Write clear, concise commit messages:
     ```bash
     git commit -m "Add feature: describe your change"
     ```
   - Push to your fork:
     ```bash
     git push origin feature/your-feature-name
     ```

5. **Open a Pull Request**:
   - Go to the original repository and create a pull request.
   - Describe your changes, including the purpose and any relevant details.
   - Reference any related issues (e.g., `Fixes #123`).

## Code Guidelines
- Use Bash for scripting to maintain compatibility with Arch Linux.
- Ensure scripts are POSIX-compliant where possible.
- Add comments to explain complex logic.
- Test with common Arch tools (`pacman`, `yay`, `flatpak`, `dialog`).

## Reporting Issues
- Use the GitHub Issues page to report bugs or suggest features.
- Include steps to reproduce, expected behavior, and actual behavior.

## Community
Join the discussion on [r/archlinux](https://reddit.com/r/archlinux) or [r/unixporn](https://reddit.com/r/unixporn) to share your `rcr` scripts and ideas!

Thank you for helping make `rcr` better!
```