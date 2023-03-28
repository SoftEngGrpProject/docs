# Installing Dependences and Libraries

Installing dependencies and libraries is a crucial step in setting up the development environment for the application. To install the necessary packages and dependencies, we will use the [**N**ode **P**ackage **M**anager](https://www.npmjs.com/) (npm).

After cloning the repository and opening the project in your code editor, open the terminal and run the following command:

```bash
npm i
```

This command will look at the `package.json` file within the repository and install all the dependencies listed in the `dependencies` and `devDependencies` sections.

Once you run the command, npm will start downloading and installing the necessary packages and modules. This process may take a few minutes depending on the size and number of packages.

After the installation is complete, npm will create a `node_modules` folder in the root directory of the project. This folder will contain all the installed packages and modules.

⚠️ It is important not to modify or delete any files in the `node_modules` folder as it may unexpected error in the application.

---