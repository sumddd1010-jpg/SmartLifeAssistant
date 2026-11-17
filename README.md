# Smart Life Assistant — Android starter project

This is a Kotlin Android Studio project scaffold for:
- Manual gig timer with a reminder 30 minutes before its entered end time.
- Zomato notification-listener starter (notification access must be enabled by the user).
- Battery threshold preference (default 25%).
- Text commands and speech-to-text commands.
- Text-to-speech output while the app is active.
- Basic one-shot alarm/reminder.
- Settings reset.
- Screenshot information screen (does not bypass Android secure-window restrictions).

## Build
1. Open this folder in Android Studio on a computer.
2. Allow Gradle sync and install Android SDK 35 if prompted.
3. Build > Build Bundle(s) / APK(s) > Build APK(s).
4. Install the generated debug APK on your Android phone.

## Important limitations / next development work
- Zomato gig end times are not guaranteed to appear in notifications. This scaffold does not log into or automate Zomato. Enter the gig end time/duration manually unless a reliable notification explicitly supplies it.
- The battery threshold is stored, but a production-ready background battery monitor/foreground service and restart handling still need to be implemented and tested. The current scaffold displays the battery level when opened.
- Background speech requires a properly implemented foreground service and notification channel. The starter sends a notification; voice is available while the app is active.
- Exact alarms may require special access on Android 12+. This starter uses an inexact-while-idle alarm for compatibility.
- Android and apps can mark screens secure. No screenshot bypass is included.
- Voice input depends on an installed Android speech-recognition provider.
- Test on the target phone and request notification permission on Android 13+.

Package: com.smartlifeassistant
Min SDK: 26 (Android 8.0)
