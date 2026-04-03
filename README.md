#  React Native Multi-Screen App (Expo)

##  Student Information
- **Name:** Norbu Dhendup  
- **Student Number:** 02230293  
- **Semester:** Software Engineering (Semester 4)

---

##  Project Title
**Practical 1: React Native Development Environment and Basic Multi-Screen Application**

---

##  Aim
To set up a React Native development environment using Expo and create a simple multi-screen mobile application with navigation.

---

##  Features
- Built using **React Native with Expo**
- File-based navigation using **Expo Router**
- Two screens:
  - Home Screen
  - About Screen
- Navigation:
  - `router.push()` → Go to another screen
  - `router.back()` → Return to previous screen
- Clean UI using **StyleSheet**

---

##  Technologies Used
- React Native  
- Expo  
- Expo Router  
- Node.js & npm  
- Visual Studio Code  

---

##  Project Structure
app/
│── layout.tsx # Navigation setup
│── index.tsx # Home Screen
│── about.tsx # About Screen
---

##  How It Works
1. App starts on **Home Screen**
2. User clicks **"Go to About"**
3. App navigates to **About Screen**
4. User clicks **"Go Back"**
5. Returns to **Home Screen**

---

##  Running the App
```bash
npm install
npm start