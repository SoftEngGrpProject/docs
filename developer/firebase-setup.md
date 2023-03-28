<!-- omit from toc -->
# Firebase Setup

<!-- omit from toc -->
## Index

- [Overview](#overview)
- [Pre-requisites](#pre-requisites)
- [Connecting the Application to Firebase](#connecting-the-application-to-firebase)
- [API Keys](#api-keys)
- [Setting up Firebase Auth](#setting-up-firebase-auth)
- [Firestore Database Setup](#firestore-database-setup)


## Overview
Firebase provides a robust backend infrastructure that can be used to build, deploy, and scale applications.

AR.it uses Firebase as its backend, and you need to connect your application to an existing Firebase project.

## Pre-requisites
- An existing Firebase project with Firestore Database enabled
- Access to the Firebase console and the project credentials (i.e. `firebaseConfig`)

## Connecting the Application to Firebase

1. Open the `App.js` file in the `app` directory of the project, and import the Firebase module at the top of the file.

```js
import firebase from 'firebase/app';
import 'firebase/firestore';
```

2. Initialise Firebase with your project credentials. You can fine your project credentials by navigating to the Firebase console and selecting your project.

```js
const firebaseConfig = {
    // Your Firebase project credentials
}

// Initializing Firebase
firebase.initializeApp(firebaseConfig);
```

3. Connect to the Firestore database by creating a new `Firestore` instance.

```js
const db = firebase.firestore();
```

4. You can now use the `db` object to read and write data to the Firestore database.

5. Make sure to import the Firebase modules in any components or modules where you plan to use it.

That's it! You have successfully connected your Social Media Application to an existing Firebase project with Firestore database enabled. You can now start using Firebase to build a backend for your application.

## API Keys
To set up Firebase for your social media application, you need to get the API keys from the Firebase Console.

1. Go to the Firebase Console and sign in to your account.
2. Select the project that you want to use for your social media application.
3. In the project dashboard, click on the gear icon located in the top left corner of the screen and select "Project settings".
4. In the project settings page, click on the "General" tab if it's not selected by default.
5. Scroll down to the "Your apps" section and select the app that you want to get the API keys for.
6. Scroll down to the "Firebase SDK snippet" section and select "Config" to view your app's configuration object.
7. Copy the configuration object to your clipboard or a text editor, as you will need to use it in your social media application's code.

Now that you have the API keys for your Firebase project, you can use them to set up the Firebase connection between your social media application and the Firebase database.

## Setting up Firebase Auth

Firebase Auth provides backend services, easy-to-use SDKs, and ready-made UI libraries to authenticate users to your app.

Setting up Firebase Authentication for the social media application is an important step to enable user authentication and authorization. Follow these steps to set up Firebase Auth:

1. Sign in to the Firebase console and select your project.
2. Click on the "**Authentication**" tab on the left-hand sidebar.
3. Click on the "**Get started**" button to enable Firebase Auth for your project.
4. Select the **Email and Password** Authentication method and click on the "**Enable**" button.
5. Once initialized, you can use the authentication method enabled to allow users to sign up, sign in, and manage their accounts within your app.
6. To secure access to protected resources within your app, such as user data, you can use Firebase's built-in security rules to define who can access what data.

With Firebase Auth set up, you can ensure that your social media app is secure and that only authorized users can access sensitive data and features.

## Firestore Database Setup

1. Navigate to the "**Firestore Database**" section and click on "**Create Database**".

2. Choose "**Start in test mode**" and select a region for your database.

3. Next, you need to set up security rules for your database.<br>
Go to the "**Rules**" tab and write the rules for your database.<br>
You can start with the following basic rules:

```lua
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if true;
    }
  }
}
```
These rules will allow all read and write requests to your database.

5. Once the rules are set up, you can start adding collections and documents to your database using the Firebase console or the Firestore API.

Now you can use the `db` object to read from and write to your Firestore database in your social media application.