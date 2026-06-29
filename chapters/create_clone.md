# Creating and Cloning Repositories

## Initializing a New Repository

```bash
git init
```

This creates a hidden `.git` directory that stores all version control data.

## Creating a Repository on GitHub

* Log in to GitHub
* Click **New Repository**
* Do not initialize with README (for CLI-first workflow)

## Cloning an Existing Repository

```bash
git clone https://github.com/username/repository.git
```

## HTTPS vs SSH

* **HTTPS**: Easy, requires PAT
* **SSH**: More secure, no repeated authentication