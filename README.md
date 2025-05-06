# DigInnoCent prjkts Manifest

This repository contains a `manifest` for syncing all backend (`b-*`) and frontend (`f-*`) projects under the [DigInnoCent](https://github.com/DigInnoCent) GitHub organization using Google's `repo` tool.

---

## 📁 Included Projects

| Type     | Projects                                                   |
|----------|------------------------------------------------------------|
| Backend  | `b-cloudmate`, `b-projectshub`, `b-pulsefin`, `b-pulsehub` |
| Frontend | `f-cloudmate`, `f-projectshub`, `f-pulsefin`, `f-pulsehub` |

---

## ⚙️ Requirements

Install the `repo` tool. It's used to manage multiple Git repositories.

### 1. Install `repo` (Linux/macOS)

```bash
mkdir -p ~/.bin
curl https://storage.googleapis.com/git-repo-downloads/repo > ~/.bin/repo
chmod a+x ~/.bin/repo

# Add to PATH
echo 'export PATH=$HOME/.bin:$PATH' >> ~/.bashrc
source ~/.bashrc   # or: source ~/.zshrc
```

---

## 🚀 Getting Started

### 2. Initialize Your Workspace

```bash
mkdir diginnocent-workspace
cd diginnocent-workspace

repo init -u https://github.com/DigInnoCent/manifest -b main
```

> This command initializes your workspace with the manifest from the `main` branch.

### 3. Sync All Projects

```bash
repo sync
```

> This will clone all linked repositories into the workspace.

---

## 📂 Directory Layout (After Sync)

```plaintext
diginnocent-workspace/
├── b-cloudmate/
├── b-projectshub/
├── b-pulsefin/
├── b-pulsehub/
├── f-cloudmate/
├── f-projectshub/
├── f-pulsefin/
└── f-pulsehub/
```

---

## 🧪 Common `repo` Commands

| Command                     | Description                           |
|-----------------------------|---------------------------------------|
| `repo sync`                 | Sync all project repositories         |
| `repo status`               | Show status of all project Git repos  |
| `repo list`                 | List all projects defined in manifest |
| `repo forall -c 'git pull'` | Pull the latest commits in all repos  |

---

## 🛠️ Workflow

* Always develop on the `dev` branch
* Push changes to the `DigInnoCent` organization repositories
* Pull requests should target `dev`

---

## 🧑‍💻 Maintainers

* [Ahmed Tohamy](https://github.com/ahmedtohamy1)
* [DigInnoCent GitHub Org](https://github.com/DigInnoCent)

---

## 📜 License

This manifest is provided for use across all DigInnoCent internal projects.
