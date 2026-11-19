# دليل بناء وتثبيت ملف APK لتطبيق ديوني (DUYOUNI)

يحتوي هذا الملف المضغوط (ZIP) على مشروع **Android Studio (Kotlin + Jetpack Compose + ML Kit + Room)** كامل وجاهز للبناء.

## الطريقة الأولى: بناء APK من الهاتف مباشرة بدون لابتوب (عبر GitHub Actions)
1. فك ضغط ملف المشروع `duyouni-android-studio-project.zip` على هاتفك.
2. افتح متصفح الهاتف (Chrome) وادخل إلى موقع **GitHub.com** وأنشئ مستودعاً جديداً (New Repository).
3. ارفع جميع الملفات والمجلدات داخل المستودع (بما فيها مجلد `.github/workflows/build-apk.yml`).
4. انتقل إلى تبويب **Actions** داخل المستودع، واضغط على **Build Duyouni Android APK** ثم **Run workflow**.
5. خلال دقيقتين تقريباً سيكتمل البناء تلقائياً على خوادم GitHub السحابية، وستجد ملف **`duyouni-debug-apk`** جاهزاً للتنزيل والتثبيت على هاتفك!

## الطريقة الثانية: البناء محلياً على هاتف Android باستخدام AndroidIDE
1. ثبّت تطبيق **AndroidIDE** على هاتفك الأندرويد.
2. فك ضغط هذا المشروع في الذاكرة الداخلية واختر فتح المجلد عبر AndroidIDE.
3. سيقوم Gradle بتنزيل المكتبات تلقائياً وبناء ملف APK لتثبيته مباشرة على نفس الهاتف.

## الطريقة الثالثة: البناء عبر Android Studio على الكمبيوتر
1. فك ضغط الملف وافتح المجلد عبر **Android Studio -> Open**.
2. انتظر انتهاء مزامنة **Gradle Sync**.
3. من القائمة العلوية اختر: **Build -> Build Bundle(s) / APK(s) -> Build APK(s)**.
4. ستجد ملف `app-debug.apk` في المسار: `app/build/outputs/apk/debug/app-debug.apk`.