# Contributing to Nox

Thank you for your interest in contributing to **Nox**! This document provides guidelines and instructions for contributing to this VS Code theme.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Setup](#development-setup)
- [Making Changes](#making-changes)
- [Submitting a Pull Request](#submitting-a-pull-request)
- [Color Palette](#color-palette)
- [Style Guidelines](#style-guidelines)
- [Reporting Issues](#reporting-issues)

## Code of Conduct

Please be respectful and considerate in all interactions. We aim to maintain a welcoming and inclusive community for everyone.

## Getting Started

1. **Fork** the repository on GitHub
2. **Clone** your fork locally:
   ```bash
   git clone https://github.com/<YOUR_USERNAME>/nox.git
   cd nox
   ```
3. **Add the upstream** repository as a remote:
   ```bash
   git remote add upstream https://github.com/joshstow/nox.git
   ```

## Development Setup

### Prerequisites

- [VS Code](https://code.visualstudio.com/) (v1.54.0 or higher)
- [Git](https://git-scm.com/)
- [Node.js](https://nodejs.org/) (for packaging)
- [vsce](https://github.com/microsoft/vscode-vsce) - VS Code Extension Manager (optional, for packaging)
  ```bash
  npm install -g @vscode/vsce
  ```

### Testing the Theme Locally

1. Open the project folder in VS Code
2. Press `F5` to open a new **Extension Development Host** window
3. The Nox theme will be automatically applied in the new window
4. Make changes to `themes/Nox-color-theme.json` and reload the window (`Cmd+R` / `Ctrl+R`) to see updates

### Testing with a Packaged Extension

You can also package the extension as a `.vsix` file for more thorough testing:

```bash
vsce package
```

This creates a `.vsix` file (e.g., `nox-0.7.1.vsix`) in the project root. Install it with:

```bash
code --install-extension nox-0.7.1.vsix
```

Or in VS Code: `Extensions` → `...` → `Install from VSIX...`

> **Note**: Only maintainers with publish access can publish to the VS Code Marketplace. If you're contributing, simply submit a PR and the maintainers will handle publishing.

### Project Structure

```
nox/
├── assets/                    # Icons, banners, and screenshots
├── themes/
│   └── Nox-color-theme.json   # Main theme definition file
├── CHANGELOG.md               # Version history
├── CONTRIBUTING.md            # This file
├── LICENSE.md                 # MIT License
├── package.json               # Extension manifest
└── README.md                  # Project readme
```

## Making Changes

1. Create a new branch for your changes:
   ```bash
   git checkout -b feature/your-feature-name
   ```
2. Make your changes to the theme file
3. Test your changes using the Extension Development Host (`F5`)

### Theme File Guidelines

- The main theme file is located at `themes/Nox-color-theme.json`
- Use the established color palette (see below) for consistency
- Add comments to explain non-obvious color choices
- Test changes across multiple file types before submitting

## Submitting a Pull Request

1. **Commit** your changes with a clear, descriptive message:
   ```bash
   git commit -m "feat: add support for Rust syntax highlighting"
   ```
2. **Push** your branch to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```
3. Open a **Pull Request** against the `main` branch
4. Fill out the PR template with:
   - A description of your changes
   - Screenshots (if applicable)
   - Related issue numbers (if applicable)

### Commit Message Convention

We follow [Conventional Commits](https://www.conventionalcommits.org/):

- `feat:` - New features or enhancements
- `fix:` - Bug fixes
- `docs:` - Documentation changes
- `style:` - Formatting changes (not CSS)
- `refactor:` - Code refactoring
- `chore:` - Maintenance tasks

## Color Palette

When contributing, please use the established Nox color palette for consistency:

| Color                                                                                                         | Hex       |
|---------------------------------------------------------------------------------------------------------------|-----------|
| <div style="width:20px;height:20px;background-color:#F92672;border:1px solid #666;border-radius:3px"></div> | `#F92672` |
| <div style="width:20px;height:20px;background-color:#AE81FF;border:1px solid #666;border-radius:3px"></div> | `#AE81FF` |
| <div style="width:20px;height:20px;background-color:#0F8ADF;border:1px solid #666;border-radius:3px"></div> | `#0F8ADF` |
| <div style="width:20px;height:20px;background-color:#66D9EF;border:1px solid #666;border-radius:3px"></div> | `#66D9EF` |
| <div style="width:20px;height:20px;background-color:#A6E22E;border:1px solid #666;border-radius:3px"></div> | `#A6E22E` |
| <div style="width:20px;height:20px;background-color:#FFDC17;border:1px solid #666;border-radius:3px"></div> | `#FFDC17` |
| <div style="width:20px;height:20px;background-color:#FD971F;border:1px solid #666;border-radius:3px"></div> | `#FD971F` |
| <div style="width:20px;height:20px;background-color:#EEFFFF;border:1px solid #666;border-radius:3px"></div> | `#EEFFFF` |
| <div style="width:20px;height:20px;background-color:#929292;border:1px solid #666;border-radius:3px"></div> | `#929292` |
| <div style="width:20px;height:20px;background-color:#1D1D1D;border:1px solid #666;border-radius:3px"></div> | `#1D1D1D` |

## Style Guidelines

- **Consistency**: Match the existing style and color usage patterns
- **Readability**: Ensure sufficient contrast between text and background
- **Minimalism**: Avoid adding unnecessary colors or overly complex highlighting

## Reporting Issues

Found a bug or have a feature request? Please [open an issue](https://github.com/joshstow/nox/issues) with:

- **Bug reports**: Include VS Code version, OS, and steps to reproduce
- **Feature requests**: Describe the enhancement and its use case
- **Language support**: Specify the language and provide sample code

## Questions?

Feel free to open an issue or reach out if you have any questions about contributing.

---

Thank you for helping make Nox better!