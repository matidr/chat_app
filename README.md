# 💬 Chat App

A Flutter app for real-time messaging and chat!  
This project focuses on **[features coming soon]** — stay tuned as the app evolves.  
It's part of my ongoing journey to strengthen my Flutter skills.  

---

## 🔮 Features

- 🔐 **Authentication Screen** — A beautiful login and signup interface with form validation.
- 🎨 **Custom Theme** — Deep purple color scheme for a modern look and feel.
- 🖼️ **Asset Management** — Integrated custom chat assets for a personalized UI.
- 🔥 **Firebase Integration** — Firebase Core and Auth configured across Android, iOS, and macOS platforms.
- 🔑 **Email/Password Authentication** — Users can sign up and log in using Firebase Authentication, with real-time error feedback via SnackBar.
- 💬 **Chat Screen** — A dedicated screen shown after successful authentication.
- 🔄 **Auth-Based Routing** — App uses `StreamBuilder` with `authStateChanges()` to automatically route users between the auth and chat screens.
- ⏳ **Splash Screen** — A loading screen displayed while the Firebase auth state is being resolved on app start.
- 🖼️ **Profile Photo Picker** — Users can capture a profile photo via the camera during signup using the `image_picker` package.
- ☁️ **Firebase Storage** — Profile photos captured during signup are uploaded to Firebase Storage and the download URL is retrieved.
- ⏺️ **Loading State** — Auth buttons are replaced with a `CircularProgressIndicator` while sign-in or sign-up is in progress.
- 🚪 **Sign Out** — Users can sign out from the chat screen via an icon button in the app bar.
- 👤 **Username on Signup** — Users enter a username during signup which is stored in Firestore alongside their email and profile image URL.
- 💬 **Message Sending** — Users can type and send messages, stored in Firestore's `chat` collection with their username and profile image.

---

## 📖 What I Learnt

This app is a work in progress — learnings will be documented as development continues:

- 🏗️ **Flutter App Structure** — Refactored the default boilerplate into a cleaner `App` widget.
- 📱 **UI Design** — Built a responsive authentication screen using `SingleChildScrollView`, `Card`, and `Form` widgets.
- 🔄 **State Management** — Implemented basic local state to toggle between Login and Signup modes.
- 🎨 **Theming** — Customized `ThemeData` with `ColorScheme.fromSeed` to maintain visual consistency.
- 🔥 **Firebase Setup** — Integrated `firebase_core` and `firebase_auth`, initialized Firebase in `main.dart` using platform-specific options.
- 🔐 **Firebase Authentication** — Implemented email/password sign-in and account creation using `FirebaseAuth`, with `FirebaseAuthException` error handling.
- 🔄 **Stream-Based Navigation** — Used `StreamBuilder` with `authStateChanges()` to reactively route users based on authentication state.
- ⏳ **Splash Screen** — Handled `ConnectionState.waiting` from the auth stream to show a loading screen during Firebase initialization.
- 📸 **Image Picker** — Integrated `image_picker` to let users capture a profile photo from the camera during signup, using `ImagePicker().pickImage()` with quality and size constraints.
- ☁️ **Firebase Storage** — Uploaded the selected profile image to Firebase Storage under `user_images/{uid}.jpg` and retrieved the download URL via `getDownloadURL()`.
- ⏺️ **Loading State** — Used an `_isAuthenticating` flag with `setState` to conditionally show a `CircularProgressIndicator` and hide action buttons during auth.
- 🔗 **Callback Pattern** — Passed an `onImagePick` callback from `AuthScreen` into `UserImagePicker` to bubble the selected `File` up to the parent widget.
- 🚪 **Sign Out** — Wired up `FirebaseAuth.instance.signOut()` to an icon button in the chat screen's `AppBar`.
- 🗄️ **Cloud Firestore** — Integrated `cloud_firestore` to store user profiles in a `users` collection and chat messages in a `chat` collection, using `Timestamp.now()` for message ordering.
- 🔗 **Firestore Reads in Widgets** — Fetched the current user's Firestore document inside an async method to attach username and image URL to each sent message.

---

## 🚀 Getting Started

1. **Clone the repo**
   ```bash
   git clone https://github.com/matidr/chat_app.git
   cd chat_app
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Run the app**
   ```bash
   flutter run
   ```

---

## 🔧 Tech Stack

- 🪄 Flutter SDK
- 📂 Dart Language
- 🔥 Firebase Core & Firebase Auth
- 📸 image_picker
- ☁️ Firebase Storage
- 🗄️ Cloud Firestore

---

## 👥 Author

**Matias Di Russo**

- LinkedIn: [Matias Di Russo](www.linkedin.com/in/matias-di-russo-2870b54b)  

---

> ✅ *Built with passion as part of my ongoing Flutter learning journey!*  
