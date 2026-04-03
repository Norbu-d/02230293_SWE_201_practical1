# Practical1App 📱

A cross-platform mobile application built with React Native, Expo, and TypeScript. This is a practical demonstration of a multi-screen navigation setup with file-based routing.

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Technology Stack](#technology-stack)
- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Getting Started](#getting-started)
- [Available Scripts](#available-scripts)
- [Architecture](#architecture)
- [Development](#development)
- [Resources](#resources)

## 🎯 Project Overview

**Practical1App** is a foundational React Native application demonstrating core concepts of modern mobile app development:
- Cross-platform compatibility (iOS, Android, Web)
- File-based routing with Expo Router
- TypeScript for type safety
- Multi-screen navigation patterns

This project serves as a learning resource for implementing navigation in React Native applications using the Expo ecosystem.

## 🛠️ Technology Stack

### Core Framework
- **React Native** (v0.81.5) - Cross-platform mobile framework
- **Expo** (v54.0.33) - Development platform and managed service
- **React** (v19.1.0) - UI library
- **TypeScript** (v5.9.2) - Type-safe JavaScript

### Navigation & UI
- **Expo Router** (v6.0.23) - File-based routing system
- **React Navigation** (v7.x) - Navigation infrastructure
  - `@react-navigation/bottom-tabs` - Tab navigation
  - `@react-navigation/native-stack` - Stack navigation
  - `@react-navigation/native` - Navigation core
  - `@react-navigation/elements` - Navigation components

### Additional Libraries
- **Expo Vector Icons** (v15.0.3) - Icon library
- **Expo Image** (v3.0.11) - Optimized image component
- **React Native Web** (v0.21.0) - Web platform support
- **React Native Gesture Handler** (v2.28.0) - Gesture support
- **React Native Reanimated** (v4.1.1) - Animation library
- **React Native Safe Area Context** (v5.6.0) - Safe area handling
- **React Native Screens** (v4.16.0) - Native screen components

### Development Tools
- **ESLint** (v9.25.0) - Code linting
- **Expo CLI** - Development server and build tools

## ✨ Features

- ✅ **Multi-screen Navigation** - Home and About screens with tab/stack navigation
- ✅ **Cross-platform Support** - Runs on iOS, Android, and Web
- ✅ **Type Safety** - Built with TypeScript for better development experience
- ✅ **File-based Routing** - Simple, intuitive routing system
- ✅ **Modern React** - Uses React 19 with latest patterns
- ✅ **Dark Mode Support** - Automatic dark/light mode switching
- ✅ **Responsive Design** - Safe area and responsive layouts
- ✅ **Linting** - ESLint configured for code quality

## 📁 Project Structure

```
Practical1App/
├── app/                      # Application source code (file-based routing)
│   ├── _layout.tsx          # Root layout component
│   ├── app.tsx              # Home screen
│   └── about.tsx            # About screen
├── assets/
│   └── images/              # App icons, splashscreen, favicon
├── app.json                 # Expo configuration
├── package.json             # Project dependencies and scripts
├── tsconfig.json            # TypeScript configuration
├── eslint.config.js         # ESLint configuration
├── expo-env.d.ts            # Expo environment types
└── README.md                # This file
```

### Key Files

| File | Purpose |
|------|---------|
| `app/_layout.tsx` | Root layout with navigation structure |
| `app/app.tsx` | Home screen component |
| `app/about.tsx` | About screen component |
| `app.json` | Expo app configuration and plugins |
| `package.json` | Dependencies, scripts, and project metadata |
| `tsconfig.json` | TypeScript compiler options |

## 🚀 Installation

### Prerequisites
- **Node.js** (v18 or higher)
- **npm** or **yarn** package manager
- **Expo CLI** (optional but recommended): `npm install -g expo-cli`

### Setup Steps

1. **Install Dependencies**
   ```bash
   npm install
   ```

2. **Verify Installation**
   ```bash
   npm run lint
   ```

## 🎮 Getting Started

### Start the Development Server

```bash
npm start
```

This launches the Expo development server with options to run on:
- **iOS Simulator**: Press `i`
- **Android Emulator**: Press `a`
- **Web Browser**: Press `w`
- **Expo Go App**: Scan QR code with the Expo Go app

### Available Platforms

```bash
# iOS Simulator (macOS only)
npm run ios

# Android Emulator
npm run android

# Web Browser
npm run web

# Custom start
npx expo start
```

## 📜 Available Scripts

| Command | Description |
|---------|-------------|
| `npm start` | Start Expo development server |
| `npm run android` | Launch Android emulator |
| `npm run ios` | Launch iOS simulator (macOS) |
| `npm run web` | Launch in web browser |
| `npm run lint` | Run ESLint to check code quality |
| `npm run reset-project` | Reset to blank slate (moves starter code to app-example) |

## 🏗️ Architecture

### Navigation Structure

The app uses **Expo Router's file-based routing** for a clean, intuitive navigation structure:

```
app/
├── _layout.tsx    (Root layout: defines overall navigation structure)
├── app.tsx        (Home screen: /index or /app)
└── about.tsx      (About screen: /about)
```

### Screen Components

**Home Screen** (`app.tsx`)
- Welcome message
- Navigation button to About screen
- Example of using `router.push()` for navigation

**About Screen** (`about.tsx`)
- Information display
- Back navigation button
- Example of using `router.back()` for navigation

## 💻 Development

### Code Style
- **TypeScript** for type safety
- **ESLint** with Expo config for code quality
- **React Native** styling with StyleSheet

### Common Development Tasks

#### Edit a Screen
```typescript
// app/screen-name.tsx
import React from 'react';
import { View, Text, Button, StyleSheet } from 'react-native';
import { useRouter } from 'expo-router';

export default function ScreenName() {
  const router = useRouter();
  return (
    <View style={styles.container}>
      {/* Your content here */}
    </View>
  );
}

const styles = StyleSheet.create({
  container: { /* ... */ },
});
```

#### Add a New Screen
1. Create a new `.tsx` file in the `app/` directory
2. Expo Router automatically creates a route for it
3. Link to it using `router.push('/screen-name')`

#### Run Linter
```bash
npm run lint
```

## 🔧 Configuration Files

### `app.json`
Contains Expo configuration including:
- App metadata (name, version, slug)
- Platform-specific settings (iOS, Android, Web)
- Splash screen and icon configuration
- Plugin configuration (Expo Router, Splash Screen)
- Experimental features (typed routes, react compiler)

### `tsconfig.json`
TypeScript compiler configuration with:
- Strict type checking enabled
- React Native and Expo type support
- Path aliases for cleaner imports

### `eslint.config.js`
ESLint configuration:
- Uses Expo's recommended ESLint config
- Enforces code quality standards

## 📚 Resources

### Official Documentation
- [Expo Documentation](https://docs.expo.dev/) - Complete Expo reference
- [Expo Router Guide](https://docs.expo.dev/router/introduction/) - File-based routing
- [React Native Docs](https://reactnative.dev/docs/getting-started) - React Native fundamentals
- [React Navigation](https://reactnavigation.org/) - Navigation library reference

### Learning Resources
- [Expo Tutorial](https://docs.expo.dev/tutorial/introduction/) - Step-by-step guide
- [Expo Snack](https://snack.expo.dev/) - Online code editor
- [React Native Community](https://react-native.community/) - Community resources

### Community
- [Expo GitHub](https://github.com/expo/expo) - Open source repository
- [Expo Discord](https://chat.expo.dev) - Community chat
- [Stack Overflow](https://stackoverflow.com/questions/tagged/react-native) - Q&A

## 🤝 Contributing & Next Steps

### Potential Enhancements
- Add more screens to expand functionality
- Implement state management (Redux, Zustand, Context API)
- Add API integration for data fetching
- Implement authentication
- Add data persistence (AsyncStorage, SQLite)
- Create custom components and themes
- Build production builds for app stores

### Building for Production

```bash
# iOS
eas build --platform ios

# Android
eas build --platform android

# Web
npm run web
```

## 📄 License

This project is part of a practical learning exercise.

---

**Last Updated:** April 1, 2026
**Framework Version:** Expo v54 | React v19 | React Native v0.81
#   0 2 2 3 0 2 9 3 _ S W E _ 2 0 1 _ p r a c t i c a l 1  
 