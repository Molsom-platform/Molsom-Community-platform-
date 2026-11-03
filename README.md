# Molsom Education Platform

React + Firebase starter for Molsom World. Features include student email/password registration and login, teacher/admin dashboard, online class links, learning material links, a searchable starter dictionary, multiple-choice exams, results and PWA install metadata.

## Firebase setup
1. Create a project at https://console.firebase.google.com.
2. Add a Web App and copy its configuration into `src/firebase.js`, replacing every `YOUR_...` placeholder.
3. In Firebase Authentication, enable the Email/Password provider.
4. Create a Cloud Firestore database.
5. Publish the rules in `firestore.rules` from Firestore Console > Rules.

## Run on Ubuntu
Install Node.js 20+ and run:
```bash
npm install
npm run dev
```
Open the local Vite URL shown in the terminal (usually http://localhost:5173).

Build:
```bash
npm run build
```

## Firebase Hosting
```bash
npm install -g firebase-tools
firebase login
firebase init hosting
```
Choose your Firebase project, set the public directory to `dist`, and configure as a single-page app. Then:
```bash
firebase deploy
```

## Vercel
Import this project folder into Vercel. Use build command `npm run build` and output directory `dist`.

## Make a teacher/admin account
New registrations are students by default. After registering the first trusted administrator, open Firestore > `users` > that user's UID document and change `role` to `admin`. For a trusted teacher use `teacher`. Never expose role editing to ordinary users.

## Android installation
Deploy with HTTPS, open the website in Chrome on Android, open the browser menu and choose **Install app** or **Add to Home screen**.

## Important production notes
- Firebase is not pre-connected. You must add your own Firebase web configuration and deploy Firestore rules.
- The included Molsom word examples are placeholders, not authoritative translations. Have fluent speakers verify all words and meanings.
- This is an advanced starter, not a fully production-audited LMS. In this sample, exam answer keys are sent to the client and scoring happens in the browser. Do not use for high-stakes exams. Move answer keys and scoring to trusted server-side code/Cloud Functions first.
- Add privacy policy, consent, account recovery, monitoring, backups, content moderation, accessibility checks and security review before public launch.

## Contact
Email: sristimolsom1234@gmail.com
Phone: 8837332788
Location: Udaipur, Gomati, Tripura
