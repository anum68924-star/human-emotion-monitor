# Human Emotion Monitor 🎭

A live Android application that monitors human emotions in real-time using the device's front camera. The app provides a live emotion score and logs detected emotions during the session.

## Features ✨

*   **Live Emotion Detection**: Real-time analysis of facial expressions.
*   **Emotion Scoring**: Provides a confidence score (0-100%) for the detected emotion.
*   **Emotion History**: A live scrolling log of recently detected emotions.
*   **Privacy-First**: All processing is done on-device using Google ML Kit; no video data is sent to any server.

## Tech Stack 🛠️

*   **Language**: Kotlin
*   **UI Framework**: Jetpack Compose
*   **Camera API**: CameraX
*   **Machine Learning**: Google ML Kit (Face Detection API)
*   **Build System**: Gradle (Kotlin DSL)

## How It Works 🧠

The app utilizes the **CameraX Image Analysis** use case to stream frames to the **ML Kit Face Detector**. 
It analyzes facial landmarks and classifications to determine:
*   **Smiling Probability**: Maps to "Happy" or "Neutral".
*   **Eye Opening Probability**: Helps detect "Surprise" or "Blinking".
*   **Real-time Scoring**: The confidence level is calculated based on the probability values returned by the ML model.

## Installation 📲

1.  Clone this repository:
    ```bash
    git clone https://github.com/YOUR_USERNAME/human-emotion-monitor.git
    ```
2.  Open the project in **Android Studio (Ladybug or newer)**.
3.  Sync Gradle and build the project.
4.  Run the app on a physical device with a front-facing camera.

## Build Output 📦

To generate the APK or AAB files:
*   **APK**: `./gradlew assembleDebug`
*   **Bundle**: `./gradlew bundleDebug`

The outputs will be located in `app/build/outputs/`.

## Permissions 🔒

This app requires:
*   `android.permission.CAMERA`: To capture live video for emotion analysis.

---
Developed as a live emotion monitoring solution.
