```markdown
# Changelog

All notable changes to Rice Cooker (`rcr`) will be documented in this file.

## [0.1.0] - 2025-08-05

### Added
- Initial release of `rcr`.
- Command logging with `-a` (last command) and `-n` (no-run).
- Comment addition with `-c`.
- Package bundling with `-b` for `arch`, `aur`, and `flatpak` categories.
- Interactive reordering with `-r` using `dialog`.
- Script editing (`-e`) and previewing (`-p`).
- Custom script path support with `-f`.
- Long option support (`--init`, `--add`, etc.) using `getopt`.

### Fixed
- Corrected reordering logic to properly swap menu items while preserving comments.
```