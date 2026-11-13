# J.A.R.V.I.S. Mark II — Android

Iron Man–inspired personal assistant for Android.

## What’s new in 2.0

| Feature | How to use it |
|--------|----------------|
| **Place calls by voice** | “Call Mom”, “Call Rahul”, “Dial 9876543210” |
| **Open any installed app** | “Open YouTube”, “Open WhatsApp”, “Launch Chrome”, “Open Camera” |
| **Contacts lookup** | Matches names in your address book, then dials |
| **Iron Man UI** | Dark HUD, cyan/gold accents, arc-reactor focus |
| **Voice + text** | Tap to speak, or type a command |
| **British-style TTS** | JARVIS replies out loud (toggleable) |

## Permissions

On first launch, allow:

- **Microphone** — voice commands  
- **Phone** — place calls directly (`CALL_PHONE`)  
- **Contacts** — resolve “call Mom” to a number  

If phone permission is denied, JARVIS still opens the **dialer** with the number filled in.

## Build an APK from your phone (GitHub Actions)

This environment cannot compile an APK. Use the included workflow:

1. Create a new GitHub repository (public or private).
2. Upload **everything inside** this `JARVIS_Android` folder, including the hidden `.github` folder.
3. Open **Actions → Build JARVIS Android APK → Run workflow**.
4. When it finishes, download the **JARVIS-debug-APK** artifact.
5. Extract and install `app-debug.apk` (allow “Install unknown apps” if asked).
6. Open JARVIS and grant microphone, phone, and contacts permissions.

## Example commands

```
call Mom
call +91 98765 43210
open YouTube
open WhatsApp
open Camera
open Settings
what time is it
what is the date
search iron man suit
help
```

## Notes

- Debug APK for testing — not a Play Store release.
- App discovery uses launcher labels; say the name as it appears on your home screen.
- Speech recognition needs a working speech service and usually a network connection.
- Background “Hey JARVIS” wake-word is not included (needs a foreground service and more setup).
- Do not put AI API keys inside the APK.
