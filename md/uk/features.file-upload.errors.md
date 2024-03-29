---
navigation:
  - features.file-upload.post-method.md: « Завантаження файлів методом POST
  - features.file-upload.common-pitfalls.md: Найпоширеніші помилки »
  - index.md: PHP Manual
  - features.file-upload.md: Завантаження файлів на сервер
title: Пояснення повідомлень про помилки
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Пояснення повідомлень про помилки

PHP повертає код помилки поряд з іншими атрибутами прийнятого файлу. Він розташований у масиві, що створюється PHP при завантаженні файлу, і може бути отриманий при зверненні по ключу `error`. Іншими словами, код помилки можна знайти в [$\_FILES\['userfile'\]\['error'\]](reserved.variables.files.md)

**`UPLOAD_ERR_OK`**

Значення: 0; Помилок не виникло, файл успішно завантажено на сервер.

**`UPLOAD_ERR_INI_SIZE`**

Значення: 1; Розмір прийнятого файлу перевищив максимально допустимий розмір, заданий директивою [upload\_max\_filesize](ini.core.md#ini.upload-max-filesize)конфигурационного файла php.ini.

**`UPLOAD_ERR_FORM_SIZE`**

Значення: 2; Розмір файлу, що завантажується, перевищив значення *MAX\_FILE\_SIZE*, вказаний у HTML-формі.

**`UPLOAD_ERR_PARTIAL`**

Значення: 3; Завантажуваний файл було отримано лише частково.

**`UPLOAD_ERR_NO_FILE`**

Значення: 4; Файл не було завантажено.

**`UPLOAD_ERR_NO_TMP_DIR`**

Значення: 6; Відсутня тимчасова папка.

**`UPLOAD_ERR_CANT_WRITE`**

Значення: 7; Неможливо записати файл на диск.

**`UPLOAD_ERR_EXTENSION`**

Значення: 8; Модуль PHP зупинив завантаження файлу. PHP не дає способу визначити, який модуль зупинив завантаження файлу; у цьому може допомогти перегляд списку завантажених модулів за допомогою [phpinfo()](function.phpinfo.md)
