# Chapter 11: GitHub

## Introduction

GitHub provides remote storage, collaboration, and backup for source code. In a professional web development workflow, every active project should have a corresponding GitHub repository. Git handles version control on your computer; GitHub makes that history durable, shareable, and recoverable.

This chapter configures GitHub for ongoing use: account setup, authentication, repository creation, and the daily commands you will use throughout development.

---

## Before You Begin

Verify that:

- Git is installed and configured (see Chapter 8).
- You have a GitHub account, or are ready to create one.
- You can sign in to GitHub in a web browser.
- Your development projects live in the Linux file system when using WSL.

---

## Step 1: Create or Verify Your GitHub Account

1. Open [https://github.com](https://github.com) in your browser.
2. Sign in, or select **Sign up** to create an account.
3. Use an email address you control and will keep long term.
4. Enable two-factor authentication (2FA) under **Settings → Password and authentication**.

Two-factor authentication is strongly recommended. It protects your repositories and reduces the risk of account compromise.

---

## Step 2: Install the GitHub CLI

The GitHub CLI (`gh`) simplifies authentication, repository creation, pull requests, and issue management from the terminal.

### On Windows (PowerShell)

```powershell
winget install --id GitHub.cli --accept-source-agreements --accept-package-agreements
```

Close and reopen your terminal after installation so `gh` is available on your PATH.

### On Ubuntu (WSL)

Follow the official installation instructions at [https://github.com/cli/cli#installation](https://github.com/cli/cli#installation), or use the package manager method recommended for your Ubuntu version.

Verify the installation:

```bash
gh --version
```

---

## Step 3: Authenticate with GitHub

Sign in once from the terminal. GitHub CLI stores credentials for 
ongoing use.

```bash
gh auth login
```

When prompted:

1. Select **GitHub.com**.
2. Select **HTTPS** as the preferred protocol for Git operations.
3. Authenticate with **Login with a web browser**.
4. Copy the one-time code displayed in the terminal.
5. Complete sign-in in the browser when prompted.

Confirm authentication:

```bash
gh auth status
```

You should see that you are logged in to `github.com`.

---

## Step 4: Configure SSH Authentication

SSH keys provide passwordless, secure authentication for Git operations. They are the preferred method for daily development.

Generate a key in the environment where you run Git most often. For WSL-based development, generate the key inside Ubuntu.

### Generate an SSH Key (WSL / Linux)

```bash
ssh-keygen -t ed25519 -C "your-email@example.com"
```

Press Enter to accept the default file location (`~/.ssh/id_ed25519`). Optionally set a passphrase for additional security.

### Add the Key to the SSH Agent

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

### Configure SSH for GitHub

Create or edit `~/.ssh/config`:

```
Host github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519
  IdentitiesOnly yes
```

### Register the Key with GitHub

Display your public key:

```bash
cat ~/.ssh/id_ed25519.pub
```

Copy the entire line, then in GitHub:

1. Open **Settings → SSH and GPG keys**.
2. Select **New SSH key**.
3. Paste the public key and save.

Alternatively, use GitHub CLI:

```bash
gh ssh-key add ~/.ssh/id_ed25519.pub --title "WSL development key"
```

Test the connection:

```bash
ssh -T git@github.com
```

You should receive a message confirming authentication. GitHub does not provide shell access; this response is expected.

---

## Step 5: Configure Git Identity

Git requires a name and email for every commit. These should match the identity you use on GitHub.

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

Verify:

```bash
git config --global user.name
git config --global user.email
```

Use the same email address associated with your GitHub account so commits appear correctly in your contribution history.

---

## Step 6: Create a GitHub Repository

Every project should have a remote repository before significant work begins.

### Option A: Create with GitHub CLI

From your project directory:

```bash
gh repo create my-project --public --source=. --remote=origin --push
```

Adjust visibility (`--public` or `--private`) as needed.

### Option B: Create on GitHub.com

1. Open [https://github.com/new](https://github.com/new).
2. Enter a repository name.
3. Do **not** initialize with a README if you already have a local repository.
4. Create the repository.
5. Connect your local repository:

```bash
git remote add origin git@github.com:USERNAME/REPO.git
git branch -M main
git push -u origin main
```

---

## Step 7: Connect an Existing Local Repository

If you initialized Git locally before creating the remote:

```bash
git remote add origin git@github.com:USERNAME/REPO.git
git push -u origin main
```

If `origin` already exists with the wrong URL:

```bash
git remote set-url origin git@github.com:USERNAME/REPO.git
```

Verify:

```bash
git remote -v
```

---

## HTTPS vs SSH

Both protocols work. Choose one and use it consistently.

| Method | Best for | Notes |
|--------|----------|-------|
| **SSH** | Daily development in WSL | Passwordless after key setup; preferred for this handbook |
| **HTTPS** | Quick setup, CI systems | Uses Git Credential Manager on Windows; works without SSH keys |

When using HTTPS on Windows, Git Credential Manager (`credential.helper=manager`) stores tokens securely after your first successful login.

When using SSH, remote URLs use the form `git@github.com:USERNAME/REPO.git`.

---

## Daily Workflow

These commands form the routine for ongoing GitHub use.

### Check Status

```bash
git status
```

### Stage and Commit Changes

```bash
git add .
git commit -m "Describe the change clearly"
```

### Push to GitHub

```bash
git push
```

On the first push of a new branch:

```bash
git push -u origin BRANCH-NAME
```

### Pull Remote Changes

```bash
git pull
```

### View Remote Repository

```bash
gh repo view --web
```

---

## Branching and Pull Requests

Use branches for features, fixes, and experiments. Keep `main` stable.

```bash
git checkout -b feature/my-change
# make changes, commit
git push -u origin feature/my-change
gh pr create
```

Review and merge pull requests on GitHub before deleting merged branches locally:

```bash
git checkout main
git pull
git branch -d feature/my-change
```

---

## Repository Organization

Adopt consistent conventions across projects:

- **One repository per application or handbook**, not one repository for everything.
- **Use descriptive commit messages** that explain why a change was made.
- **Push regularly** so work is backed up on GitHub.
- **Keep secrets out of Git** — never commit passwords, API keys, or `.env` files with credentials.
- **Add a `.gitignore`** appropriate to your stack before the first commit.

---

## GitHub CLI Commands for Ongoing Use

| Command | Purpose |
|---------|---------|
| `gh auth status` | Confirm you are signed in |
| `gh repo create` | Create a new repository |
| `gh repo view --web` | Open the repository in a browser |
| `gh repo clone USER/REPO` | Clone a repository |
| `gh pr create` | Open a pull request |
| `gh pr list` | List open pull requests |
| `gh issue list` | List issues |
| `gh ssh-key add` | Register an SSH public key |

---

## Windows and WSL Considerations

When using WSL as your primary development environment:

- Generate SSH keys **inside WSL**, not only on Windows.
- Store projects in the Linux file system (for example, `~/projects/`), not under `/mnt/c/`.
- Run `git`, `gh`, and `ssh` from the same environment consistently.
- If you also use Git on Windows, maintain separate SSH keys or configure both environments deliberately to avoid confusion.

Cursor integrates with WSL. Open projects from the Linux path so Git operations run in the correct environment.

---

## Common Problems

### `Permission denied (publickey)`

- Confirm your SSH public key is registered on GitHub.
- Verify `~/.ssh/config` points to the correct private key.
- Run `ssh-add ~/.ssh/id_ed25519` if the agent is not loaded.

### `Repository not found`

- Confirm the repository exists on GitHub.
- Verify the remote URL: `git remote -v`.
- Confirm your account has access to the repository.

### `Support for password authentication was removed`

GitHub no longer accepts account passwords for Git operations. Use SSH keys or a personal access token with HTTPS.

### Commits show the wrong author

- Check `git config user.name` and `git config user.email`.
- Ensure the email matches your GitHub account.

### Line ending warnings on Windows

Git for Windows may convert line endings. For cross-platform projects, add a `.gitattributes` file and commit it early:

```
* text=auto
```

---

## Best Practices

- Enable two-factor authentication on your GitHub account.
- Use SSH for daily Git operations in WSL.
- Install and authenticate GitHub CLI once; reuse it for repository and pull request management.
- Push commits at the end of each work session.
- Write commit messages that describe intent, not just file names.
- Never commit secrets or local configuration with credentials.
- Keep `main` deployable; use branches for work in progress.

---

## Chapter Checklist

Before continuing, confirm that:

- You have a GitHub account with two-factor authentication enabled.
- GitHub CLI is installed and `gh auth status` reports a successful login.
- An SSH key is generated and registered with GitHub.
- `ssh -T git@github.com` confirms authentication.
- Git `user.name` and `user.email` are configured.
- Your project has a remote named `origin` pointing to the correct repository.
- You can push and pull without errors.

Once these items are complete, GitHub is configured for ongoing use.

---

## Looking Ahead

With Git, GitHub, Node.js, and Cursor in place, your development environment supports the full lifecycle of modern web projects: writing code, versioning changes, collaborating through pull requests, and maintaining reproducible project history across machines.
