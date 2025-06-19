# Emoji-Pass

**Your face is your password.** Emoji-Pass turns facial expressions into a sequence of emojis you “type” by snapping photos with your webcam.

---

## Features

- **Camera-On-Click**  
  Clicking any password field opens your webcam inline—no separate dialog.

- **Face → Emoji Mapping**  
  Uses [face-api.js](https://github.com/justadudewhohacks/face-api.js) to detect your dominant expression (happy, sad, angry, etc.) and maps it to a corresponding emoji.

- **Backspace-Only Editing**  
  Password fields are `readonly` except for Backspace, so you can only remove emojis, never type letters or numbers.

- **Login & Sign-Up Workflows**  
  - **Sign-Up:** enter username, build an emoji-sequence in both password fields, submit.  
  - **Login:** enter username, re-build your emoji-sequence, submit.  
  Both forms validate presence and (for sign-up) matching emoji sequences.

- **Modern UI & Glassmorphism**  
  Frosted-glass card, gradient background, smooth slider tabs, and minimalist controls.

---

## Flow

1. **Choose Tab**  
   Toggle between **Login** and **Sign Up** via slider tabs.

2. **Enter Username**  
   Type in your desired username.

3. **Open Camera**  
   Click the password field. The camera container appears above the tabs.

4. **Take Photo**  
   Hit **📸 Take Photo**. The app snaps a frame, runs expression detection, and appends the mapped emoji to that field.

5. **Build Sequence**  
   Repeat “Open Camera → Take Photo” as many times as you like to form your emoji-sequence password.

6. **Submit**  
   - **Sign Up:** checks that both password fields have at least one emoji and match.  
   - **Login:** checks that you’ve recorded at least one emoji.

7. **Feedback**  
   You get an alert confirming success or describing any missing steps.

---

## Usage

1. Clone or download the repo.  
2. Place the `weights/` folder (from face-api.js) alongside `index.html`.  
3. Open `index.html` in any modern browser.  
4. Follow the flow above to sign up and log in with emoji-passwords.

---

## File Structure
├── index.html ← markup, camera & face-api logic
├── style.css ← glassmorphic styling & layout
└── weights/ ← face-api.js model files


---

## Customization

- **Emoji Map:** edit the `emojiMap` object in `index.html` to change expression→emoji mappings.  
- **UI Styles:** tweak `style.css` for different gradients, blur levels, or form styles.  
- **Models:** swap in your own face-api.js weights or host them from another path.

---

## License

This project is released under the MIT License. See **LICENSE** for details.  