# طقس MCNC (MCNC Weather - Monorepo) 🇸🇾🌦️
### المستودع الرئيسي الشامل للمركز الوطني للأرصاد الجوية والمناخ في الجمهورية العربية السورية

يضم هذا المستودع تطبيقين مستقلين تماماً للأرصاد الجوية والمناخ باللغة العربية، تم بناء وهيكلة كل منهما كـ Sub-Project منفصل تماماً في ملفات البناء والاعتماديات والاختبارات.

---

## 📁 الهيكل العام للمستودع (Project Architecture)

```
new-app/
├── android_native/                 # تطبيق أندرويد الأصيل (Kotlin + Jetpack Compose)
│   ├── app/
│   │   ├── src/main/java/          # الكود البرمجي بـ Kotlin (MVVM / Compose)
│   │   ├── src/main/res/           # الصور، الأيقونات والنصوص العربية
│   │   ├── src/test/               # اختبارات الوحدات (Robolectric Tests)
│   │   └── build.gradle.kts
│   ├── build.gradle.kts
│   ├── settings.gradle.kts
│   └── README.md                   # توثيق وطريقة تشغيل نسخة Kotlin
│
├── flutter_app/                    # تطبيق فلاتر العابر للمنصات (Flutter + Dart)
│   ├── lib/
│   │   ├── main.dart               # نقطة البداية وإعدادات RTL العربية
│   │   ├── config/                 # إعدادات الـ APIs والتطبيق
│   │   ├── models/                 # نماذج البيانات (المحطات، CAP، التوقعات)
│   │   ├── repositories/           # مستودعات البيانات والربط بـ Open-Meteo
│   │   ├── services/               # خدمات الطقس والمساعد الذكي
│   │   ├── screens/                # الشاشات الرئيسية
│   │   ├── widgets/                # مكونات الواجهة الزجاجية M3
│   │   └── theme/                  # الألوان والتصميم المظلم
│   ├── assets/                     # الأصول والأيقونات
│   ├── test/                       # اختبارات الوحدات بـ Dart
│   ├── pubspec.yaml                # حزم واعتماديات Flutter
│   └── README.md                   # توثيق وطريقة تشغيل نسخة Flutter
│
├── shared_docs/                    # التوثيق المعماري الموحد للمشروعين
│   ├── architecture/
│   ├── api/
│   ├── database/
│   ├── deployment/
│   └── development/
│
├── .github/workflows/              # أنابيب التشييد والاختبار المستمر (CI/CD)
│   ├── android-ci.yml              # فحص واختبار نسخة Kotlin
│   └── flutter-ci.yml              # فحص واختبار نسخة Flutter
│
└── README.md                       # التوثيق الرئيسي للمستودع
```

---

## 📱 التطبيق الأول: Android Native (Kotlin)
- **المسار:** `android_native/`
- **التقنيات:** Kotlin 2.2+, Jetpack Compose, Material Design 3, Coroutines, Retrofit, Robolectric.
- **طريقة التشغيل والتجربة:**
  ```bash
  cd android_native
  ./gradlew assembleDebug
  ./gradlew testDebugUnitTest
  ```

---

## 💙 التطبيق الثاني: Cross-Platform (Flutter)
- **المسار:** `flutter_app/`
- **التقنيات:** Flutter 3+, Dart 3+, Material Design 3 (Dark Glassmorphism), Arabic RTL.
- **طريقة التشغيل والتجربة:**
  ```bash
  cd flutter_app
  flutter pub get
  flutter analyze
  flutter test
  flutter run
  ```

---

## 📡 مصادر البيانات ونظام CAP
- **بيانات الطقس والتوقعات:** ربط مباشر بـ Open-Meteo API.
- **تنبيهات طوارئ الطقس (CAP):** ربط موثق كواجهة تكامل خارجية مع مشروع [Meteo CAP Warning System](https://github.com/meteo2026net-oss/cap) عبر نقطة النهاية المفتوحة `/api/public/alerts`.
