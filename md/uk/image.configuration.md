---
navigation:
  - image.installation.md: « Установка
  - image.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - image.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Image Опції налаштування**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [gd.jpegignorewarning](image.configuration.md#ini.gd.jpeg-ignore-warning) | "1" | PHPINIALL |  |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`gd.jpeg_ignore_warning` bool

Ігнорувати попередження(але не помилки), згенеровані libjpeg(-turbo).

**Список змін для `gd.jpeg_ignore_warning`**

| Версия | Описание |
| --- | --- |
|  | Значення gd.jpegignorewarning за замовчуванням змінено з 0 на 1. |

Дивіться також директиви налаштування [exif](exif.configuration.md)

**Увага**

Функції для роботи із зображеннями споживають багато пам'яті. Переконайтеся, що значення [memorylimit](ini.core.md#ini.memory-limit) досить велике, якщо використовуєте штатну бібліотеку GD.
