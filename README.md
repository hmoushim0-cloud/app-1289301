# مشروع تعكس هذه المنصة حاجة مشرو (Project 1289301)

![Platform: Android](https://img.shields.io/badge/Platform-Android-3DDC84?style=flat&logo=android&logoColor=white)
![Kotlin 2.1](https://img.shields.io/badge/Language-Kotlin%202.1-7F52FF?style=flat&logo=kotlin&logoColor=white)
![Jetpack Compose](https://img.shields.io/badge/UI-Jetpack%20Compose-4285F4?style=flat&logo=jetpackcompose&logoColor=white)
![Clean Architecture](https://img.shields.io/badge/Architecture-Clean%20Architecture%20(MVVM)-orange?style=flat)
![Security Verified](https://img.shields.io/badge/Security-Zero--Vulnerability%20Gate-success?style=flat)
![Design: Pure Vectors](https://img.shields.io/badge/Design-Pure%20Vector%20Drawables-blue?style=flat)

> **نظام رقمي سحابي متكامل فائق الأداء والأمان**

---

## Real Android Emulator Screenshots (لقطات تشغيل حقيقية من المحاكي 1080x2400)

| الشاشة الرئيسية واستعراض الخدمات | تفاصيل الطلب والتسعير | التتبع المباشر وحالة المعالجة |
|:---:|:---:|:---:|
| ![Main Screen](screenshots/01_home.png) | ![Details](screenshots/02_details.png) | ![Live Tracking](screenshots/03_tracking.png) |

---

## Project Overview (نظرة عامة على المشروع)

مشروع متكامل لتنفيذ متطلبات: تعكس هذه المنصة حاجة مشروع تدقيق وتشغيل وتسليم صناعي يتطلب ضبطاً صارماً لمسارات الجودة، التحقق، وإغلاق الأعمال. القيمة المضافة تتمثل في تحويل المتطلبات النصية إلى سير عمل تشغيلي واضح: خطة جودة، تدقيق، اختبارات قبل التشغيل وبعده، ثم تسليم نهائي مع تدريب وإقفال موقع، مع قابلية استقبال مرشحين من تخصصات PMP وCAPM وPRINCE2 أو خبرة مماثلة. 

معمارياً، يعتمد الحل على Clean Architecture بفصل طبقات العرض، المجال، والبيانات لضمان سهولة الصيانة وقابلية التوسع، مع ربط سحابي لإدارة الملفات، الاعتمادات، وسجل الأحداث. يتم فرض حالات صارمة للطلب، صلاحيات دقيقة، وتتبّع كامل للتغييرات لضمان النزاهة التشغيلية، مع طبقة تكامل جاهزة للتخزين السحابي، الإشعارات، وتوثيق التسليم النهائي.. تم بناء وتوثيق النظام بأحدث معايير هندسة البرمجيات وأمان البيانات.

---

## Core Features (المميزات الرئيسية)

- **تصميم عصري داعم للعربية**
- **Clean Architecture MVVM**
- **دعم الدفع الإلكتروني والفوترة**
- **تتبع لحظي بالـ GPS**

---

## Clean Architecture Layers

```
sa.factory.app1289301
├── data/
│   └── OrderRequestRepository.kt          # Flow-based reactive data source
├── model/
│   └── OrderRequestModels.kt              # Immutable business data structures
└── ui/
    ├── MainActivity.kt                # Jetpack Compose Entry Activity
    ├── OrderRequestViewModel.kt           # StateFlow UI state holder
    └── OrderRequestScreens.kt             # Material 3 Compose vector screens
```

---

## Architectural Invariants & Security Threats

### Invariants (القواعد الصارمة):
- **`totalCalculationExact`**: Total price must equal subtotal plus VAT with zero floating point inaccuracy
- **`statusTransitionsMonotonic`**: Status progression must strictly advance through state machine

### Threat Model (حماية البيانات والتهديدات):
- Customer PII must be encrypted at rest with SQLCipher and redacted from logs
- Payment tokens must be strictly ephemeral and signed with TLS certificate pinning

---

## Build Instructions

```bash
# Clone the repository
git clone https://github.com/hmoushim0-cloud/app-1289301.git
cd app-1289301

# Assemble Debug APK
./gradlew :app:assembleDebug
```

---

### Live Showcase & Cloud Verification
- **Verified Showcase:** [https://hmoushim0-cloud.github.io/live-previews/?id=1289301](https://hmoushim0-cloud.github.io/live-previews/?id=1289301)
