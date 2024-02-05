---
navigation:
  - ref.pdo-ibm.connection.md: « PDO\_IBM DSN
  - ref.pdo-informix.connection.md: PDO\_INFORMIX DSN »
  - index.md: PHP Manual
  - pdo.drivers.md: Драйвери PDO
title: Функції Informix (PDO\_INFORMIX)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Функції Informix (PDO\_INFORMIX)

## Вступ

PDO\_INFORMIX – це драйвер, що реалізує інтерфейс [PHP Data Objects (PDO)](intro.pdo.md) для доступу до бази даних Informix.

## Установка

Для складання модуля PDO\_INFORMIX знадобиться встановлений на тому ж хості Informix Client SDK 2.81 UC1 або вище. Informix Client SDK можна завантажити з [» сайту підтримки IBM Informix](http://www-306.ibm.com/software/data/informix/tools/csdk/)

PDO\_INFORMIX є модулем [» PECL](https://pecl.php.net/), так что для его установки следуйте следующим инструкциям[Встановлення модулів PECL](install.pecl.md). Виконайте команду **configure** вказавши місцезнаходження заголовкових файлів та бібліотек Informix Client SDK:

```
bash$ ./configure --with-pdo-informix=/path/to/SDK[,shared]
```

По умолчанию команда**configure** буде використовувати значення змінної оточення INFORMIXDIR.

## Перемотується курсор

PDO\_INFORMIX підтримує курсори, що перемотуються; проте за умовчанням їх використання не дозволено. Для дозволу їхньої підтримки ви повинні вказати **`ENABLESCROLLABLECURSORS=1`** у відповідних налаштуваннях з'єднання ODBC в odbc.ini або встановити параметр \*\*`EnableScrollableCursors=1`\*\*в строке соединения (DSN).

## Зміст

-   [PDO\_INFORMIX DSN](ref.pdo-informix.connection.md)— З'єднання з базою даних Informix
