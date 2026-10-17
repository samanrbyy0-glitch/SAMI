ساخت APK (روی ویندوز/مک/لینوکس)

پیش‌نیازها:
1) Node.js (نسخه LTS) از nodejs.org
2) Android Studio از developer.android.com/studio  (JDK و Android SDK همراهش نصب می‌شود؛ یک‌بار بازش کن تا SDK دانلود شود)

مراحل (داخل پوشه‌ی همین پروژه، در ترمینال):
  npm install
  npx cap add android
  npx cap sync android

ساخت فایل APK:
  روش ۱ (ساده): npx cap open android  → در Android Studio منوی Build > Build APK(s)
  روش ۲ (ترمینال):  cd android  &&  ./gradlew assembleDebug   (ویندوز: gradlew.bat assembleDebug)

فایل خروجی:
  android/app/build/outputs/apk/debug/app-debug.apk
آن را به گوشی بفرست و نصب کن (اجازه‌ی «نصب از منبع ناشناس» لازم است).

بعد از نصب:
- اولین بار اجازه‌ی نوتیفیکیشن را بده.
- اگر اندروید پرسید، اجازه‌ی «Alarms & reminders» را هم بده.
- برای دقیق‌بودن الارم، بهینه‌سازی باتری را برای این اپ خاموش کن (Settings > Apps > لیست روزانه > Battery > Unrestricted).
- بعد از ریستارت گوشی یک‌بار اپ را باز کن تا الارم‌ها دوباره تنظیم شوند.

تغییر ساعت‌ها: داخل اپ روی ساعت هر کار بزن؛ الارم‌ها خودکار دوباره تنظیم می‌شوند.
