# Installing and Configuring Git

## Installing Git

**Linux (Debian/Ubuntu):**

```bash
sudo apt update
sudo apt install git
```

**macOS (Homebrew):**

```bash
brew install git
```

**Windows:**
Download Git from the official website and install it with default options.

## Verifying Installation

```bash
git --version
```

## Initial Configuration

Git requires your identity for commits.

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## Setting Default Branch Name

```bash
git config --global init.defaultBranch main
```

## Viewing Configuration

```bash
git config --list
```

---