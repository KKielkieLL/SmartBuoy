# React Native Project Setup with Firebase and AWS

This guide walks you through setting up a React Native project using Expo, configuring Firebase and AWS, and testing it on an emulator with a 6.7-inch screen size.

---

## **1. Install an Emulator (6.7-inch Screen Size)**

### **Steps for Installing Android Studio Emulator**
1. **Download and Install Android Studio**  
   - Visit the [Android Studio website](https://developer.android.com/studio) and download the installer.
   - Follow the installation instructions for your operating system.
2. **Set Up the Emulator**  
   - Open Android Studio and navigate to `AVD Manager` (`Tools > Device Manager`).
   - Create a new Virtual Device:
     - Select a phone profile like "Pixel 4 XL" or any device with a similar screen size (6.7 inches).
     - Choose a system image (e.g., API Level 30 or above).
     - Set the resolution to match a 6.7-inch screen (1440 x 3200 recommended).
   - Start the emulator to ensure it works properly.

---

## **2. Create a React Native Project Using Expo**

1. **Install Expo CLI**  
   ```
   npm install -g expo-cli
Initialize a New Project


expo init my-project
cd my-project
Choose the "blank" template when prompted.
Start the Expo Development Server


expo start
Test the app on the emulator by selecting the Android option.
3. Install Firebase and AWS
Install Firebase


npm install firebase
Install AWS SDK


npm install aws-sdk
4. Set Up Firebase
Create a Firebase Project
Go to the Firebase Console and create a new project.
Add a Web App
Register your app and copy the Firebase configuration object.
Set Up Firebase in the Project
In your React Native project, create a firebaseConfig.js file:
javascript

import { initializeApp } from "firebase/app";

const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_AUTH_DOMAIN",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_STORAGE_BUCKET",
    messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
    appId: "YOUR_APP_ID",
};

const app = initializeApp(firebaseConfig);
export default app;
Install Firebase Firestore (Optional)
If using Firestore:


npm install @firebase/firestore
5. Test the App
Run the App on Emulator



expo start
Select the Android emulator to view your app.

Debug Errors
If there are any issues, check the console logs or Expo Debugger.

6. Save and Push to Repository
Save your progress and optionally push to GitHub:


git init
git add .
git commit -m "Initial project setup with Firebase and AWS"
git branch -M main
git remote add origin https://github.com/yourusername/my-project.git
git push -u origin main
