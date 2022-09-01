---
navigation:
  - exif.requirements.md: « Вимоги
  - exif.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - exif.setup.md: Встановлення та налаштування
title: Встановлення
---
## Встановлення

Щоб увімкнути підтримку exif, налаштуйте PHP з опцією **\-enable-exif**

Користувачі Windows повинні увімкнути DLL-файли phpmbstring.dll та phpexif.dll у php.ini. DLL phpmbstring.dll повинна бути завантажена *до* DLL phpexif.dll, так що налаштуйте ваш php.ini відповідним чином.
