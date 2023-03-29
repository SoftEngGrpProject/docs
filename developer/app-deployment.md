# App Deployment

App deployment is a critical process in bringing an application to the hands of the users.

With [Expo CLI](https://expo.dev/tools#cli), deploying an app is made easier and more streamlined. To deploy the social media application via [Expo CLI](https://expo.dev/tools#cli), the `expo eject` command must be used.<br>
This command will generate native project files that can be built, signed, and submitted to the respective app stores.

❗Before using the `expo eject` command, ensure that the app is fully functional and free of any bugs.

Once the app is ready for deployment, navigate to the project directory in the terminal and run the following command:

```bash
expo eject
```

This command will generate native project files for both iOS and Android platforms. The generated files will be stored in a newly created directory called `ios` and `android`, respectively.

After generating the native project files, navigate to the `ios` directory and open the `project_name.xcworkspace` file in Xcode. From here, the app can be built, signed, and submitted to the App Store for review and eventual release.

For Android, navigate to the `android` directory and open the project in Android Studio. Build the app, generate a signed APK file, and submit the APK to the Google Play Store for review and release.

Overall, using the `expo eject` command streamlines the app deployment process and makes it easier to release the app to the respective app stores.