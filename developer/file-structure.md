<!-- omit from toc -->
# File Structure
<!-- omit from toc -->
## Table of Contents

- [Overview](#overview)
- [`app` directory](#app-directory)
  - [`assets` directory](#assets-directory)
  - [`components` directory](#components-directory)
  - [`functions` directory](#functions-directory)
  - [`redux` directory](#redux-directory)


## Overview
The file structure is the codebase of AR.it . It is organized in a way that makes it easy to navigate and understand. The file structure is as follows:

```
.
├── app
│   ├── App.js
│   ├── app.json
│   ├── assets
│   │   ├── adaptive-icon.png
│   │   ├─ ...
│   │   └── splash.png
│   ├── babel.config.js
│   ├── components
│   │   ├── Main.js
│   │   ├── assets
│   │   ├── auth
│   │   │   ├── Captcha.js
│   │   │   ├── Confirmation.js
│   │   │   ├─  ...
│   │   │   └── checkEmail.js
│   │   ├── core
│   │   │   └── theme.js
│   │   ├── elements
│   │   │   ├── BackButton.js
│   │   │   ├── Background.js
│   │   │   ├─  ...
│   │   │   └── TextInputWithLable.js
│   │   ├── main
│   │   │   ├── Add.js
│   │   │   ├─  ...
│   │   │   └── editProfile.js
│   │   └── styles
│   │       └── styles.js
│   ├── functions
│   │   ├── firebase.json
│   │   └── functions
│   │      ├── index.js
│   │      └─  ...
│   ├── package-lock.json
│   ├── package.json
│   ├── redux
│   └── yarn.lock
├── node_modules
└── package-lock.json
```

## `app` directory
The `app` directory contains the source code of the application, where the `App.js` file serves as the entry point of the application.

The `app.json` file contains the configuration options of the app.

The `package.json` file contains information about the dependencies of the application, and the `yarn.lock` and `package-lock.json` files contain the exact version of each dependency.

### `assets` directory

The `assets` directory contains the assets of the application, such as images, fonts, and icons.

### `components` directory

The `components` directory contain subdirectories such as `auth`, `core`, `elements`, `main`, and `styles`.

Each of these subdirectories contains reusable components that can be used throughout the application.

The `auth` directory contains the components that are used in the authentication process such as login, register, forgot password, and others.

The `core` directory contains the components that are used in the core of the application such as the theme.

The `elements` directory contains the common UI components that are used throughout the application such as buttons, text inputs and headers.

The `main` directory contains the main screen components in the application such as the feeds, profiles, and others.

The `styles` directory contains the styles for all the components in the application.

### `functions` directory

The `functions` directory contains the source code of all the Firebase Cloud Functions used in the application, such as sending notifications and verifying users.

### `redux` directory

The `redux` directory contains the source code of the Redux store and related files.

---
