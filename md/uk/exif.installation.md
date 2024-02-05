---
navigation:
  - exif.requirements.md: « Вимоги
  - exif.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - exif.setup.md: Встановлення та налаштування
title: Установка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка

Щоб увімкнути підтримку exif, налаштуйте PHP з опцією **\--enable-exif**

Користувачі Windows повинні увімкнути DLL-файли php\_mbstring.dll та php\_exif.dll у php.ini. DLL php\_mbstring.dll повинна бути завантажена *до*DLL php\_exif.dll, так що налаштуйте ваш php.ini відповідним чином.
