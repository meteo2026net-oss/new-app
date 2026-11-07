# طقس MCNC (MCNC Weather - Kotlin Android Version) 🇸🇾🌦️
### التطبيق الرسمي للمركز الوطني للأرصاد الجوية والمناخ في الجمهورية العربية السورية (نسخة كوتلن الأصيلة)

تطبيق متطور وعالي الدقة يوفر توقعات الطقس الآنية والمستقبلية لجميع المحافظات السورية والعالم، مبني باستخدام أحدث تقنيات أندرويد الرسمية.

---

## 🛠️ التقنيات المستخدمة (Tech Stack)
- **اللغة:** Kotlin 2.2+
- **واجهة المستخدم:** Jetpack Compose (Material Design 3 - Dark Glassmorphism)
- **إدارة الحالة:** ViewModel + StateFlow / Coroutines
- **شبكة البيانات والـ APIs:** Retrofit + Moshi (Open-Meteo REST API)
- **الخرائط:** WebView + Leaflet.js Weather Radar
- **الاختبارات:** Robolectric Unit Tests

---

## 🌟 الميزات الأساسية
1. **شبكة محطات الرصد السورية (13 محطة رسمية):** دمشق الدولي، حلب الدولي، اللاذقية البحرية، حمص، طرطوس، حماة، دير الزور، القامشلي، السويداء، درعا، إدلب، الرقة، وتدمر.
2. **بروتوكول الإنذار المبكر (CAP Alerts):** تنبيهات العواصف، الأمطار الغزيرة وموجات الحر.
3. **النشرة الجوية الصوتية (Audio Bulletin):** مع إمكانية تحويل النص إلى كلام (Android TTS).
4. **توقعات الطقس الدقيقة:** 24 ساعة ساعية و 7 أيام تفصيلية عبر Open-Meteo.
5. **مؤشرات البيئة والطقس (8 بطاقات):** الرطوبة، سرعة واتجاه الرياح، الضغط الجوي، مؤشر الأشعة UV، جودة الهواء AQI، الرؤية الأفقية، الحرارة المحسوسة، وحبوب اللقاح.
6. **مساعد الطقس الذكي (MCNC Assistant):** نصائح اللباس والسفر والإرشادات الزراعية.
7. **لوحة تحكم الأرصاد (Admin Dashboard):** بث التنبيهات وتحديث النشرة الصوتية.

---

## 🚀 كيفية التشغيل والرفع إلى GitHub
```bash
# البناء والاختبار عبر Gradle
./gradlew assembleDebug
./gradlew testDebugUnitTest

# الرفع لمستودع meteo-wheather الخاص بـ Kotlin
git init
git add .
git commit -m "feat: Official MCNC Weather Kotlin Native App"
git branch -M main
git remote add origin https://github.com/meteo2026net-oss/meteo-wheather.git
git push -u origin main
```
