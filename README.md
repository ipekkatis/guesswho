# 🎭 Guess Who? — Personalized Edition
 
Create your own **Guess Who** game with custom characters and photos. Share with friends using a simple code — no app, no account needed.
 
**[▶ Play Now](https://guesswho-personalized.vercel.app)**
 
---
 
## Features
 
- **Custom characters** — add up to 50 characters with names and photos
- **Two-code system** — a Play code to share with friends, an Edit code to update your game
- **Public games** — publish your game so anyone can discover and play it
- **Personal fork** — friends can edit their own copy without affecting the original
- **Secret character** — a random character is picked at the start for each player
- **4 themes** — Purple Night, Warm Gold, Deep Ocean, Rose Pink
- **No install** — runs entirely in the browser, single HTML file
## How to Use
 
### Create a game
1. Click **Create New Game**
2. Add characters (name + photo URL or upload)
3. Choose a theme and privacy setting
4. Click **Generate Code** — you get two codes:
   - 🎮 **Play Code** (`GW-XXXXX`) — share this with friends
   - ✎ **Edit Code** (`GE-XXXXX`) — keep this private, use it to update the game
### Play a game
- Enter a **Play Code** on the home screen
- Eliminate characters by clicking the ✕ button
- Use the 👁 button to reveal your secret character
### Edit a game
- Enter your **Edit Code** — takes you directly to the editor
- Make changes and click **Save Changes**
- The public game updates instantly for everyone
## Tech Stack
 
- Vanilla HTML / CSS / JavaScript (single file, no build step)
- [Firebase Firestore](https://firebase.google.com/) for game storage
- Google Fonts (Bebas Neue + DM Sans)
## Self-hosting
 
1. Clone this repo
2. Create a [Firebase project](https://console.firebase.google.com/) and enable Firestore
3. Replace the Firebase config in `index.html` with your own
4. Deploy anywhere — GitHub Pages, Netlify, Vercel, or just open the file locally
## Firestore Rules
 
```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /games/{gameId} {
      allow read: if true;
      allow write: if true;
    }
  }
}
```
 
---
 
Made with ♥ — feel free to fork and customize.
