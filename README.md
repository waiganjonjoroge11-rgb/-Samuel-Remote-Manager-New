# Student Movement Tracker

A separate web application for school transport movement. It is independent of Samuel Remote Manager and is designed to use its own Firebase project, login and Firestore database.

## Features
- Separate morning pickup and afternoon drop-off statuses per student and date.
- Transported, Absent and Pending statuses.
- Date, timestamp and staff email recorded for each change.
- Student register, class filter, search, daily totals and CSV history export.
- Email/password login; no public sign-up.

## One-time activation still required
1. Create a new Firebase project only for Student Movement Tracker. Do not reuse the Samuel Remote Manager Firebase project.
2. Add a Firebase Web App and copy apiKey, authDomain, projectId and appId.
3. Enable Email/Password Authentication and create authorised staff accounts.
4. Create Cloud Firestore and publish the rules from firestore.rules.
5. Replace the PASTE_ values in index.html under firebaseConfig with the Firebase web-app values.
6. Configure GitHub Pages to use GitHub Actions in repository Settings > Pages.

Only signed-in users can access student records. All authenticated accounts currently share the same access level; role-specific permissions need additional configuration. Removing a student retains their historical records. Device timestamps are saved as ISO date-time values. Keep student information confidential.
