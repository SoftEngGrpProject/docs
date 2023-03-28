<!-- omit from toc -->
# Firebase Setup

<!-- omit from toc -->
## Index

- [Overview](#overview)
- [Pre-requisites](#pre-requisites)
- [Connecting the Application to Firebase](#connecting-the-application-to-firebase)
- [API Keys](#api-keys)


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