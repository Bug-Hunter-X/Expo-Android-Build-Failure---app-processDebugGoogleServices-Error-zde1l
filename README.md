# Expo Android Build Failure: :app:processDebugGoogleServices

This repository demonstrates a common error encountered when building Android apps with Expo CLI. The build process fails with the error `:app:processDebugGoogleServices` due to issues with the `google-services.json` configuration file.

## Problem

The `google-services.json` file is essential for integrating Firebase services into your Android app. If this file is missing, improperly formatted, or contains incorrect configuration, the build will fail. This issue is usually resolved by ensuring that a properly configured `google-services.json` file exists within the `android/app` directory of your Expo project.

## Solution

The solution involves ensuring the presence and proper configuration of the `google-services.json` file.  This usually requires retrieving the file from the Firebase console and placing it correctly in the Android project directory. The file should be downloaded from the Firebase project settings for your app.

## Steps to Reproduce (Bug)

1. Create a new Expo project.
2. Attempt to build an Android APK without including a `google-services.json` file in the `android/app` directory. 
3. Run `expo build:android`.
4. Observe the error `:app:processDebugGoogleServices`.

## Steps to Resolve (Solution)

1. Log in to the Firebase console.
2. Locate your project.
3. Download the `google-services.json` file.
4. Place the `google-services.json` file into the `android/app` directory of your Expo project.
5. Run `expo build:android` again.

The solution demonstrates the crucial role of the `google-services.json` file in the Expo Android build process.  Make sure your `google-services.json` file is correctly configured with your Firebase project information to avoid these errors.