# ⚛️ React Native Project Setup Guide (Windows)

A complete step-by-step guide to set up and run your **React Native** app on **Windows** — including all Java, Android, and SDK configurations.

---

## 🧩 1. Prerequisites

Make sure the following tools are installed **before** creating your project 👇

| 🛠️ Tool | 💡 Description | 🔗 Download |
|----------|----------------|-------------|
| **Node.js (LTS)** | JavaScript runtime environment | [nodejs.org](https://nodejs.org/) |
| **npm** | Comes with Node.js | *(auto installed)* |
| **Java JDK 17 / 21** | Required for Android builds | [adoptium.net](https://adoptium.net/) |
| **Android Studio** | Includes SDK, emulator, and build tools | [developer.android.com/studio](https://developer.android.com/studio) |
| **Git** | Used for fetching dependencies | [git-scm.com](https://git-scm.com/) |

---

## ⚙️ 2. Android Setup

### 🧭 Step 1: Install Android SDK

1. Open **Android Studio** → *More Actions* → **SDK Manager**
2. Make sure these are installed:
   - ✅ Android SDK Platform 34 (or latest)
   - ✅ Android SDK Command-line Tools
   - ✅ Android SDK Build-Tools
   - ✅ NDK (Recommended: `27.2.12479018`)

---

### ⚡ Step 2: Configure Environment Variables

Go to  
**System Properties → Environment Variables → New**

| Variable Name | Path Example |
|----------------|--------------|
| `JAVA_HOME` | `C:\Program Files\Eclipse Adoptium\jdk-17` |
| `ANDROID_HOME` | `C:\Users\kamekazi\AppData\Local\Android\Sdk` |

Then, edit the **Path** variable and add:


✅ Test everything:
```bash
java -version
adb --version
```
```bash
npx @react-native-community/cli init myApp
cd myApp
npm install
```
```bash
adb devices
```

Configure Local Properties android/local.properties

```bash
sdk.dir=C:\\Users\\kamekazi\\AppData\\Local\\Android\\Sdk
ndk.dir=C:\\Users\\kamekazi\\AppData\\Local\\Android\\Sdk\\ndk\\27.2.12479018
```

.\gradlew clean

```bash
npx react-native run-android
```
