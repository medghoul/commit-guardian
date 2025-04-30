# 🔄 husky-setup

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![npm version](https://img.shields.io/npm/v/husky-setup.svg?style=flat)](https://www.npmjs.com/package/husky-setup)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

> Universal Git hooks setup script for Node.js projects

A zero-configuration script that automatically sets up Git hooks for code quality assurance in any Node.js project. This script dynamically adapts to your Node.js version and project structure, intelligently configuring [Husky](https://github.com/typicode/husky), [ESLint](https://eslint.org/), [Prettier](https://prettier.io/), and [Commitlint](https://commitlint.js.org/) as needed.

## 🚀 Features

- **Universal Compatibility**: Works with any Node.js version (10+)
- **Zero Configuration**: Detects and installs appropriate package versions for your environment
- **Smart Detection**: Intelligently detects existing tools in your project
- **Adaptive Installation**: Only installs what's missing
- **Flexible Hooks**: Creates hooks that work properly in any environment
- **Non-Blocking Workflow**: ESLint errors won't block commits (configurable)
- **Conventional Commits**: Enforces consistent commit message format

## 🛠️ Quick Install

### Option 1: Direct Download and Run

```bash
# Download and execute the script
curl -o- https://raw.githubusercontent.com/username/husky-setup/main/husky-setup.sh | bash

# Or with wget
wget -qO- https://raw.githubusercontent.com/username/husky-setup/main/husky-setup.sh | bash
```

### Option 2: npm Installation

```bash
# Global installation
npm install -g husky-setup
cd your-project
husky-setup

# Or as a dev dependency
npm install --save-dev husky-setup
npx husky-setup
```

### Option 3: Manual Download

```bash
# Clone the repository
git clone https://github.com/username/husky-setup.git

# Copy the script to your project
cp husky-setup/husky-setup.sh your-project/

# Make it executable and run
cd your-project
chmod +x husky-setup.sh
./husky-setup.sh
```

## 🎯 What It Does

This script:

1. **Detects** Node.js and npm versions
2. **Checks** for ESLint and Prettier in your project
3. **Offers** to install missing tools
4. **Installs** version-appropriate dependencies
5. **Configures** Husky for Git hooks
6. **Creates** basic config files if needed
7. **Sets up** pre-commit and commit-msg hooks
8. **Updates** your README with hook information

## 📌 Git Hooks Included

| Hook | Function | Notes |
|------|----------|-------|
| **pre-commit** | Runs Prettier and ESLint before each commit | ESLint errors shown as warnings by default |
| **commit-msg** | Validates commit message format | Follows [Conventional Commits](https://www.conventionalcommits.org/) |

## 📝 Commit Message Format

This setup enforces the [Conventional Commits](https://www.conventionalcommits.org/) format:
