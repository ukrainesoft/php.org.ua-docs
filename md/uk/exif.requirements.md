---
navigation:
  - exif.setup.md: '" Встановлення та налаштування'
  - exif.installation.md: Встановлення »
  - index.md: PHP Manual
  - exif.setup.md: Встановлення та налаштування
title: Вимоги
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Вимоги

Ваш PHP має бути скомпільований з опцією `--enable-exif`. Для включення підтримки багатобайтових кодувань у тегах EXIF ​​необхідно увімкнути модуль [mbstring](ref.mbstring.md). Включити його можна, скомпілювавши PHP з опцією `--enable-mbstring`

Тільки для Windows: модуль [mbstring](ref.mbstring.md) завжди має бути включений. Зверніть увагу, що модуль [mbstring](ref.mbstring.md) повинен завантажуватись раніше, ніж EXIF ​​(черговість у php.ini).
