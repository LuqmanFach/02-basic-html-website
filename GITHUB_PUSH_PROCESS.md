# How to Push a Project to GitHub

## Prerequisites

- Git installed on your computer
- GitHub CLI (gh) installed

---

## Step 1: Install GitHub CLI (First time only)

```bash
winget install GitHub.cli
```

## Step 2: Authenticate with GitHub

```bash
gh auth login
```

Follow the prompts:

1. Select "GitHub.com" → Press Enter
2. Choose "HTTPS" → Press Enter
3. Type "Y" to authenticate
4. Choose "Login with a web browser"
5. Enter the one-time code shown in terminal
6. Complete authentication in browser

Verify login:

```bash
gh auth status
```

## Step 3: Initialize Git Repository

Navigate to your project folder:

```bash
cd path/to/your/project
```

Initialize git:

```bash
git init
```

## Step 4: Add Files to Staging

Add all files:

```bash
git add .
```

Or add specific files:

```bash
git add filename.html
```

## Step 5: Create Initial Commit

```bash
git commit -m "Initial commit - your message here"
```

## Step 6: Create Remote Repository and Push

Create repository and push in one command:

```bash
gh repo create repository-name --public --source=. --push
```

Or separate steps:

```bash
# Create the repository
gh repo create repository-name --public

# Add remote
git remote add origin https://github.com/username/repository-name.git

# Push to GitHub
git push -u origin master
```

---

## Additional Commands

### Check status

```bash
git status
```

### Check remote

```bash
git remote -v
```

### Push changes

```bash
git push
```

### Pull changes

```bash
git pull
```

### View repositories

```bash
gh repo list
```
