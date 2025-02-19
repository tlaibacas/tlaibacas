# 👋 Hi, I'm Tiago!

![Banner](https://your-image-url.com) <!-- Replace with your image URL -->

## About Me

Hello! I'm **Tiago**, a **React and JavaScript Developer** with a passion for building web applications. I specialize in both **frontend** and **backend** development, using a modern tech stack. I'm always learning and improving my skills to create high-quality projects.

### 🖥️ Languages I Know

- JavaScript
- TypeScript
- HTML
- CSS
- Node.js
- SQL
- Python

### ⚙️ Tools I Use

- React, Next.js
- Node.js, Express
- MongoDB, MySQL
- Git, GitHub, VSCode
- Figma, Adobe XD

### 🚀 Current Project

Currently, I am working on a **project management web app** built with **React** and **Node.js**, where users can track tasks, collaborate with teams, and manage deadlines. The project is in the **development phase** and I’m actively working on improving the UI and adding features.

### 📊 GitHub Stats

#### 📅 Number of Commits

To display the number of commits in a repository, we can use the GitHub API to fetch this information dynamically. Here’s a basic example:

```javascript
fetch('https://api.github.com/repos/tiago-laibacas/your-repo/commits')
  .then(response => response.json())
  .then(commits => {
    console.log(`Total commits: ${commits.length}`);
  });
