# المخطط المعماري الموحد لتطبيقي طقس MCNC (MCNC Weather)

يقدم هذا التوثيق البنية المعمارية المعتمدة لكلا النسختين (Kotlin Native و Flutter Cross-Platform).

## 1. نمط التصميم (Architecture Pattern)
- **Android Native:** Clean Architecture + MVVM (Model-View-ViewModel) باستعمال StateFlow و Jetpack Compose.
- **Flutter:** Clean Architecture مقسمة مجلداتها بحسب المسؤوليات:
  - `config`: الثوابت ونقاط الاتصال الخارجية.
  - `models`: كائنات البيانات وقاموس الحقول.
  - `repositories`: طبقة إدارة وترشيح البيانات.
  - `services`: شبكة الاتصال بالـ REST APIs.
  - `widgets` / `screens`: واجهة المستخدم RTL M3.

## 2. التكامل مع النظام الخارجي للانذار المبكر (CAP)
- يتم استهلاك تنبيهات CAP الجوية من مشروع [CAP Warning System](https://github.com/meteo2026net-oss/cap) الملازم عبر نقطة النهاية العامة `/api/public/alerts`.
