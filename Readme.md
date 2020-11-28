# Setup for OTA React Native CLI Using AppCenter

## Setup SDK AppCenter (Android)
1. Add the SDK to the project
    - npm install appcenter appcenter-analytics appcenter-crashes --save-exact
2. Integrate the SDK
    - Create a new file with the filename appcenter-config.json in android/app/src/main/assets/ with the following content:
    > {
    >    "app_secret": "YOUR_APP_SECRET"
    > }
3. Modify the app's res/values/strings.xml to include the following lines:   
    > <string name="appCenterCrashes_whenToSendCrashes" moduleConfig="true" ?translatable="false">DO_NOT_ASK_JAVASCRIPT</string>
    ><string name="appCenterAnalytics_whenToEnableAnalytics" moduleConfig="true" translatable="false">ALWAYS_SEND</string>
4. Explore data
    - Now build and launch your app, then go to the Analytics section. You should see one active user and at least one session! The charts will get more relevant as you get more users. Once your app actually crashes, you will have Crashes data show up as well.

#### dev

