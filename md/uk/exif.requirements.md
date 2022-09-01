---
navigation:
  - exif.setup.html: « Встановлення та налаштування
  - exif.installation.html: Установка »
  - index.html: PHP Manual
  - exif.setup.html: Встановлення та налаштування
title: Вимоги
---
## Вимоги

Ваш PHP має бути скомпільований з опцією `--enable-exif`. Для включення підтримки багатобайтових кодувань у тегах EXIF ​​необхідно увімкнути модуль [mbstring](ref.mbstring.md). Включити його можна, скомпілювавши PHP з опцією `--enable-mbstring`

Тільки для Windows: модуль [mbstring](ref.mbstring.html) завжди має бути включений. Зверніть увагу, що модуль [mbstring](ref.mbstring.md) повинен завантажуватись раніше, ніж EXIF ​​(черговість у php.ini).
