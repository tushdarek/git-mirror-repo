# Git Mirror Repository (GitLab → GitHub)

This project demonstrates how to mirror a repository from **GitLab to GitHub**, ensuring that both repositories stay automatically synchronized.

Whenever changes are pushed to the GitLab repository, the same commits are automatically pushed to the GitHub repository using **GitLab Push Mirroring**.

---

# 📌 Project Overview

Repository mirroring allows developers to keep repositories on different platforms synchronized.

In this project:

* GitLab is used as the **primary repository**
* GitHub acts as the **mirror repository**
* Every commit pushed to GitLab is automatically mirrored to GitHub

This setup helps maintain **backup repositories, cross-platform collaboration, and redundancy**.

---

# 🚀 Features

* Automatic synchronization between GitLab and GitHub
* Backup repository for redundancy
* Cross-platform repository availability
* Simple configuration using GitLab mirroring feature

---

# 🛠 Technologies Used

* Git
* GitLab
* GitHub
* GitLab Push Mirroring
* Personal Access Tokens (PAT)

---

# 📂 Project Workflow

```
Developer
   │
   ▼
GitLab Repository (Primary)
   │
   ▼
Push Mirroring
   │
   ▼
GitHub Repository (Mirror)
```

Every push to GitLab automatically appears in GitHub.

---

# ⚙️ Implementation Steps

## 1️⃣ Create a GitHub Repository

1. Login to GitHub
2. Click **New Repository**
3. Provide repository name
4. Initialize with a **README.md**
5. Create repository

---

## 2️⃣ Generate GitHub Personal Access Token

Go to:

```
GitHub → Settings → Developer Settings → Personal Access Tokens
```

Click:

```
Generate New Token (Classic)
```

Select permission:

```
repo
```

Copy the token because it will be used as a password during mirror configuration.

---

## 3️⃣ Create a GitLab Project

1. Login to GitLab
2. Click **New Project**
3. Select **Blank Project**
4. Enter project name
5. Initialize with README
6. Create project

---

## 4️⃣ Configure Repository Mirroring

Navigate to:

```
Project → Settings → Repository → Mirroring Repositories
```

Click **Mirror Repository**

Enter the GitHub repository URL:

```
https://<GITHUB_USERNAME>@github.com/<GITHUB_USERNAME>/<REPOSITORY>.git
```

Set mirror direction:

```
Push
```

---

## 5️⃣ Authenticate with GitHub Token

Enter the credentials:

```
Username : GitHub Username
Password : GitHub Personal Access Token
```

Save the mirror configuration.

Now GitLab will automatically push changes to GitHub.

---

## 6️⃣ Clone Repository and Push Code

Clone the GitLab repository:

```bash
git clone https://gitlab.com/<GITLAB_USERNAME>/<REPOSITORY>.git
cd <REPOSITORY>
```

Create a sample file:

```bash
touch index.html
```

Add content:

```html
<h1>This is my mirror repo project</h1>
```

Commit and push:

```bash
git add index.html
git commit -m "Add index.html file"
git push -u origin main
```

---

# ✅ Verification

1. Push code to GitLab repository
2. Open GitHub repository
3. The same file will automatically appear

This confirms that **GitLab → GitHub mirroring is working successfully**.

---

# 📌 Benefits of Repository Mirroring

* Repository backup
* High availability of code
* Cross-platform collaboration
* Easy migration between platforms

---

# 🎯 Conclusion

By configuring **GitLab Push Mirroring**, the GitLab repository becomes the **source of truth**, while GitHub automatically receives updates.

This setup provides an automated and reliable way to keep repositories synchronized across platforms.

---

# 📄 License

This project is created for **learning and demonstration purposes**.
