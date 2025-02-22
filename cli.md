# 🚀 Useful Expo Development Commands

This document contains essential Expo CLI commands for development, debugging, and troubleshooting.

## 📌 Essential Expo Commands

### 1️⃣ Clean and Rebuild Native Code
```sh
npx expo prebuild --clean
```
- **Use when:** You need to regenerate `android` and `ios` native folders from scratch (e.g., after changing dependencies that affect native code).
- **Warning:** This **deletes** and **recreates** your native project, so any manual modifications in `android/` or `ios/` will be lost.

### 2️⃣ Run App on a Physical iOS Device
```sh
npx expo run:ios --device
```
- **Use when:** You want to build and install the app on a real iOS device (not a simulator).
- **Requires:** A Mac with Xcode installed and an Apple Developer account.

### 3️⃣ Completely Uninstall App from iOS Simulator
```sh
xcrun simctl uninstall booted com.yourappname
```
- **Use when:** You need to completely remove the app from the iOS simulator to clear stored data (e.g., reset SQLite database, AsyncStorage, etc.).

### 4️⃣ Start Expo and Clear Cache
```sh
expo start --clear
```
_or_
```sh
npx expo start -c
```
- **Use when:** You encounter weird caching issues or need a fresh start without old builds interfering.
- **Effect:** Clears Metro bundler cache and forces Expo to rebuild the project.

## 🔥 Quick Guide on When to Use These
| Command | When to Use |
|---------|------------|
| `npx expo prebuild --clean` | Need to regenerate native code after dependency changes. |
| `npx expo run:ios --device` | Running on a real iOS device. |
| `xcrun simctl uninstall booted com.yourappname` | Fully reset the app on the iOS simulator (clears SQLite, AsyncStorage, etc.). |
| `expo start --clear` / `npx expo start -c` | Clear cache and ensure fresh project build. |

---

📌 **To contribute or suggest additional commands, feel free to submit a pull request!** 🚀

