
https://youtu.be/TW02hwhBvo4?si=zqiH9HprVkkDWA4h

1.Open console of firebase
2.Create project 
3.Give the name and location
4.Open authentication add email password
5.Open Dashboard
6.add app use App check
7.open firebase database 
8.change rules 
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /users/{userId} {
      allow read, update, delete: if request.auth != null && request.auth.uid == userId;
      allow create: if request.auth != null;
    }
  }
}
