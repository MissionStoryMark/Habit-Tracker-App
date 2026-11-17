# Daybreak Streaks

A tiny personal habit tracker. Add the things you want to do every day, hold one down until it is full (or tap its circle fast), and watch the streak grow. Holding charges the row from left to right with a rising hum and buzz; the pop comes with a chime, a glow, stardust and a rumble. Long streaks open portals to new colour worlds. Each habit can have its own celebration: up to three emojis and a picture that fly across the screen in place of the stardust. Streak milestones (1, 3, 7, 14, 21, 30, 50, 100, 365 days…) get a full-screen celebration.

## Files

- `index.html` – the whole app (markup, styles and script, no build step)
- `manifest.webmanifest`, `sw.js`, `icon.svg`, `icons/` – what lets a phone install it to the home screen and open it offline

## Put it on your phone

Host this folder on any static host (GitHub Pages, Vercel, Netlify), open the address on your phone, then:

- iPhone: Safari → Share → Add to Home Screen
- Android: Chrome → menu → Add to Home screen / Install app

Your habits are saved on the phone itself, in the browser's storage for that address.

## Vibration

Android uses the Vibration API, so the buzz builds during a hold. iPhones have no vibration API for web pages: Safari only gives a haptic tap when a finger flips a switch control (iOS 17.4 and later), so each habit circle and the opening screen sit on an invisible switch, and tapping the circle is the way to feel the charge build.

## Sound

All sound is synthesised with Web Audio, no files. The app asks iOS for the `playback` audio session so it is heard with the silent switch on; the speaker button mutes it.
