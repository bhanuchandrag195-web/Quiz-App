# Simple Quiz App

A minimal Android app (Java) demonstrating a single-question quiz:
TextView question, RadioGroup answers, Submit/Reset buttons, and
result feedback ("Correct!" / "Incorrect!").

## Open & Run

1. Open Android Studio -> **Open** -> select the `SimpleQuizApp` folder.
2. Let Gradle sync (Android Studio will download the Gradle distribution
   and dependencies on first sync — internet connection required).
3. Click **Run** ▶ on an emulator or connected device.

## Build an APK manually

```
./gradlew assembleDebug
```
The APK will be at `app/build/outputs/apk/debug/app-debug.apk`.

## Note on the Gradle wrapper

`gradle/wrapper/gradle-wrapper.jar` (a binary file) is not included.
Android Studio will offer to regenerate it automatically on first sync.
If using the command line and `./gradlew` fails with a "wrapper jar not
found" error, run (with Gradle installed locally):

```
gradle wrapper --gradle-version 8.4
```

## Project structure

```
SimpleQuizApp/
├── app/
│   ├── build.gradle
│   └── src/main/
│       ├── AndroidManifest.xml
│       ├── java/com/example/simplequizapp/MainActivity.java
│       └── res/
│           ├── layout/activity_main.xml
│           ├── values/ (strings, colors, themes)
│           ├── drawable/ (launcher icon shapes)
│           ├── mipmap-anydpi-v26/ (adaptive icons)
│           └── xml/ (backup rules)
├── build.gradle
├── settings.gradle
└── gradle.properties
```

## Customizing the question

Edit `CORRECT_ANSWER` and the RadioButton labels/question text in
`MainActivity.java` and `activity_main.xml`.
