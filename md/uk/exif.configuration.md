---
navigation:
  - exif.installation.md: « Установка
  - exif.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - exif.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

Exif підтримує автоматичне перетворення кодувань символів Unicode і JIS користувальницьких коментарів, коли модуль [mbstring](ref.mbstring.md) доступний. При цьому коментар спочатку декодується за допомогою вказаного набору символів. Потім результат кодується в іншому наборі символів, який має збігатися з вашим `HTTP`висновком.

**Опції конфігурації Exif**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [exif.encodeunicode](exif.configuration.md#ini.exif.encode-unicode) | "ISO-8859-15" | PHPINIALL |  |
| [exif.decodeunicodemotorola](exif.configuration.md#ini.exif.decode-unicode-motorola) | "UCS-2BE" | PHPINIALL |  |
| [exif.decodeunicodeintel](exif.configuration.md#ini.exif.decode-unicode-intel) | "UCS-2LE" | PHPINIALL |  |
| [exif.encodejis](exif.configuration.md#ini.exif.encode-jis) | "" | PHPINIALL |  |
| [exif.decodejismotorola](exif.configuration.md#ini.exif.decode-jis-motorola) | "JIS" | PHPINIALL |  |
| [exif.decodejisintel](exif.configuration.md#ini.exif.decode-jis-intel) | "JIS" | PHPINIALL |  |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`exif.encode_unicode` string

`exif.encode_unicode` визначає набір символів UNICODE при обробці коментарів користувача. За замовчуванням це ISO-8859-15, який має працювати для більшості неазіатських країн. Ця установка може бути порожньою або повинна бути кодуванням, що підтримується mbstring. Якщо воно порожнє, використовується поточне внутрішнє кодування mbstring.

`exif.decode_unicode_motorola` string

`exif.decode_unicode_motorola` визначає внутрішнє кодування символів зображення для Unicode-кодованих коментарів користувача, якщо зображення має байтовий порядок motorola (big-endian). Ця установка не може бути порожньою, але ви можете вказати список кодувань, які підтримуються mbstring. Типово UCS-2BE.

`exif.decode_unicode_intel` string

`exif.decode_unicode_intel` визначає внутрішнє кодування символів зображення для Unicode-кодованих коментарів користувача, якщо зображення має байтовий порядок intel (little-endian). Ця установка не може бути порожньою, але ви можете вказати список кодувань, які підтримуються mbstring. Типово UCS-2LE.

`exif.encode_jis` string

`exif.encode_jis` визначає набір символів JIS для обробки коментарів користувача. За промовчанням - порожнє значення, яке змушує функції використовувати поточне внутрішнє кодування mbstring.

`exif.decode_jis_motorola` string

`exif.decode_jis_motorola` визначає внутрішнє кодування символів зображення для JIS-кодованих коментарів, якщо зображення має байтовий порядок motorola (big-endian). Ця установка не може бути порожньою, але ви можете вказати список кодувань, які підтримуються mbstring. Типово JIS.

`exif.decode_jis_intel` string

`exif.decode_jis_intel` визначає внутрішнє кодування символів зображення для JIS-кодованих коментарів користувача, якщо зображення має байтовий порядок intel (little-endian). Ця установка не може бути порожньою, але ви можете вказати список кодувань, які підтримуються mbstring. Типово JIS.
