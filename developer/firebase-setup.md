<!-- omit from toc -->
# Firebase Setup

<!-- omit from toc -->
## Index

- [Overview](#overview)
- [Pre-requisites](#pre-requisites)
- [Connecting the Application to Firebase](#connecting-the-application-to-firebase)


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