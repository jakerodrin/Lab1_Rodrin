# Laboratory Exercise 1: Git, GitHub, and Branching
  
**Student Name:** Rodrin  
**Repository:** [Lab1_Rodrin](https://github.com/jakerodrin/Lab1_Rodrin)

---

## 📌 Project Overview
This repository contains the dynamic webpage developed for Laboratory Exercise 1. It demonstrates basic web development (HTML, CSS, JavaScript) alongside essential Git version control concepts, including multi-branch management and remote GitHub integration.

---

## 🛠️ Step-by-Step Implementation Guide

### **Step 1: Configure Git Identity**
Configured global Git credentials to ensure commits are properly attributed to the author.
```bash
git config --global user.name "jakerodrin"
git config --global user.email "jakerodrin4@gmail.com"
```

---

### **Step 2: Initialize Local Repository**
Created the local project directory and initialized Git version control.
```bash
git init
```

---

### **Step 3: Create HTML-Only Base Version & Commit**
Created `index.html` with basic document structure and staged only the HTML file for the initial commit.
```bash
git add index.html
git commit -m "Initial commit: HTML only"
```

---

### **Step 4: Rename Branch & Connect Remote GitHub Repository**
Renamed the default branch to `main`, cleared existing stored credentials, linked the local repository to GitHub, and pushed the base HTML version.
```bash
git branch -M main
echo "url=https://github.com" | git credential reject
git remote add origin https://github.com/jakerodrin/Lab1_Rodrin.git
git push -u origin main
```

---

### **Step 5: Create and Push `no-style` Branch**
Created a separate branch named `no-style` to preserve the unstyled, HTML-only version of the project.
```bash
git branch no-style
git push origin no-style
```

---

### **Step 6: Add CSS Styling, JS Interactivity & Push Final Main Version**
Created `style.css` and `script.js`, linked them inside `index.html`, staged all files, committed the additions, and updated the `main` branch.
```bash
git add .
git commit -m "Add CSS styling and JS interactivity"
git push origin main
```

---

## 🌿 Branch Summary

| Branch Name | Content / Description |
| :--- | :--- |
| **`main`** | Complete dynamic webpage containing `index.html`, `style.css`, and `script.js`. |
| **`no-style`** | Preserved baseline version containing only unstyled `index.html`. |
