# 🛡️ EmpowHer

### A Personal Safety & Emergency Assistance Android Application

**EmpowHer** is an Android-based women safety application designed to provide quick access to emergency assistance and safety tools. The application combines **SOS alerts, location services, emergency contacts, shake detection, fake calls, and Firebase** to help users respond quickly in potentially unsafe situations.

---

## ✨ Features

### 🚨 SOS Emergency Assistance

* Quickly trigger an emergency SOS action.
* Uses the device's location capabilities to support emergency assistance.
* Designed for situations where the user needs immediate help.

### 📍 Location Services

* Accesses the user's current location.
* Uses Google Maps and Google Location Services.
* Helps provide location information during emergency situations.

### 📱 Emergency Communication

* Supports emergency communication using phone and SMS capabilities.
* Allows the application to interact with emergency contacts.

### 📳 Shake Detection

* Detects device shaking using the phone's sensors.
* Can be used as an alternative way to activate safety functionality when interacting with the screen may not be convenient.

### 📞 Fake Call

* Provides a fake incoming-call interface.
* Can be used as a personal safety tool to help the user leave an uncomfortable or potentially unsafe situation.

### 👤 User Authentication & Profile

* User signup and login functionality.
* Profile management.
* User information can be stored and managed using Firebase services.

### ☁️ Firebase Integration

* Firebase Authentication for user authentication.
* Firebase Realtime Database for storing application data.
* Firebase Analytics integration.

---

## 🛠️ Tech Stack

| Technology                     | Usage                                     |
| ------------------------------ | ----------------------------------------- |
| **Java**                       | Android application development           |
| **Android SDK**                | Mobile application platform               |
| **AndroidX**                   | Modern Android components                 |
| **Firebase Authentication**    | User authentication                       |
| **Firebase Realtime Database** | Data storage                              |
| **Firebase Analytics**         | Application analytics                     |
| **Google Maps SDK**            | Maps and location visualization           |
| **Google Location Services**   | Device location                           |
| **Google Places SDK**          | Places and location-related functionality |
| **RecyclerView**               | Displaying dynamic lists                  |
| **Material Components**        | UI components                             |
| **Gradle Kotlin DSL**          | Project build configuration               |

The current project configuration targets **Android SDK 35**, with a minimum supported SDK of **24**, and uses Java 11 compatibility.

---

## 🏗️ Project Structure

```text
EmpowHer/
│
├── app/
│   ├── src/
│   │   ├── androidTest/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com/example/womensafety/
│   │   │   │       ├── Contact.java
│   │   │   │       ├── EditProfileActivity.java
│   │   │   │       ├── FakeCallActivity.java
│   │   │   │       ├── HelperClass.java
│   │   │   │       ├── LoginActivity.java
│   │   │   │       ├── ProfileActivity.java
│   │   │   │       ├── ShakeDetector.java
│   │   │   │       ├── SignupActivity.java
│   │   │   │       └── SosActivity.java
│   │   │   │
│   │   │   ├── res/
│   │   │   └── AndroidManifest.xml
│   │   │
│   │   └── test/
│   │
│   ├── build.gradle.kts
│   └── proguard-rules.pro
│
├── gradle/
├── build.gradle.kts
├── gradle.properties
├── gradlew
├── gradlew.bat
└── settings.gradle.kts
```

The repository currently contains dedicated activities for authentication, profile management, SOS, fake calls, and related safety functionality.

---

## 🔐 Permissions

The application uses Android permissions required for its safety-related functionality, including:

* Internet access
* Fine and coarse location
* Background location
* Contacts
* SMS
* Phone state
* Phone calls
* Vibration
* Device sensors

These permissions are declared in the application's `AndroidManifest.xml`.

> **Privacy Note:** Users should grant permissions only when required and understand how location, contacts, SMS, and phone functionality are used by the application.

---

## 🚀 Getting Started

### Prerequisites

Make sure you have:

* Android Studio
* Android SDK
* JDK 11 or compatible Java environment
* A Firebase project
* An Android device or emulator

---

### 1. Clone the Repository

```bash
git clone https://github.com/ashish070patel/EmpowHer.git
```

```bash
cd EmpowHer
```

---

### 2. Open in Android Studio

Open the cloned project using **Android Studio** and allow Gradle to synchronize the project.

---

### 3. Configure Firebase

Create a Firebase project and connect the Android application to it.

Download your Firebase configuration file:

```text
google-services.json
```

and place it inside:

```text
app/
└── google-services.json
```

The project is configured with the Google Services Gradle plugin and Firebase Authentication/Realtime Database dependencies.

---

### 4. Configure Google Maps

Set up a Google Maps API key according to the Android Maps SDK requirements.

Make sure the required Google Maps and location services are enabled for your Firebase/Google Cloud project.

---

### 5. Build the Application

From Android Studio:

```text
Build → Make Project
```

or use Gradle:

```bash
./gradlew build
```

On Windows:

```bash
gradlew.bat build
```

---

### 6. Run the Application

Connect an Android device or start an emulator and press:

```text
Run ▶
```

in Android Studio.

---

## 🔄 Application Flow

```text
                ┌───────────────┐
                │    EmpowHer   │
                └───────┬───────┘
                        │
                        ▼
                ┌───────────────┐
                │ Signup / Login│
                └───────┬───────┘
                        │
                        ▼
                ┌───────────────┐
                │ User Profile  │
                └───────┬───────┘
                        │
             ┌──────────┼──────────┐
             ▼          ▼          ▼
          ┌─────┐   ┌───────┐  ┌─────────┐
          │ SOS │   │ Shake │  │Fake Call│
          └──┬──┘   │Detect │  └─────────┘
             │      └───┬───┘
             │          │
             └────┬─────┘
                  ▼
          ┌───────────────┐
          │ Location /    │
          │ Emergency     │
          │ Communication │
          └───────────────┘
```

---

## 🎯 Purpose

EmpowHer aims to provide a simple and accessible collection of personal safety tools in one Android application.

The project focuses on:

* Faster access to emergency actions
* Location-aware safety assistance
* Simple emergency communication
* Alternative interaction through device shaking
* Personal safety tools such as fake calls
* Secure user authentication and profile management

---

## 🔮 Future Improvements

Potential improvements include:

* [ ] Trusted emergency contact management
* [ ] Automatic SOS countdown
* [ ] Live location sharing
* [ ] Real-time emergency tracking
* [ ] Push notifications
* [ ] Improved background SOS handling
* [ ] Emergency contact verification
* [ ] Offline emergency functionality
* [ ] Improved accessibility
* [ ] Multi-language support
* [ ] Safety tips and awareness resources
* [ ] Better privacy controls
* [ ] Emergency event history

---

## 🧪 Testing

The project includes Android instrumentation tests and unit-test configuration through Gradle.

Before releasing a production version, test:

* Authentication
* Location permissions
* SOS functionality
* SMS/phone functionality
* Shake detection
* Firebase connectivity
* Google Maps functionality
* Background location behavior
* Permission denial scenarios

---

## ⚠️ Important Disclaimer

EmpowHer is intended as a **personal safety assistance tool** and should not be considered a replacement for emergency services.

Users should contact the appropriate local emergency services when facing an immediate threat.

The reliability of features such as location, SMS, phone calls, and background services can depend on:

* Device hardware
* Android version
* Network availability
* GPS availability
* Application permissions
* Battery-saving restrictions
* Operating-system policies

---
