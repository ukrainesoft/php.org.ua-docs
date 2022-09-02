---
navigation:
  - ref.pdo-ibm.connection.md: « PDOIBM DSN
  - ref.pdo-informix.connection.md: PDOINFORMIX DSN »
  - index.md: PHP Manual
  - pdo.drivers.md: Драйвери PDO
title: Функції Informix (PDOINFORMIX)
---
# Функції Informix (PDOINFORMIX)

## Вступ

PDOINFORMIX – це драйвер, що реалізує інтерфейс [PHP Data Objects (PDO)](intro.pdo.md) для доступу до бази даних Informix.

## Встановлення

Для складання модуля PDOINFORMIX знадобиться встановлений на тому ж хості Informix Client SDK 2.81 UC1 або вище. Informix Client SDK можна завантажити з [» сайта поддержки IBM Informix](http://www-306.ibm.com/software/data/informix/tools/csdk/)

PDOINFORMIX є модулем [» PECL](https://pecl.php.net/), так що для його встановлення дотримуйтесь наступних інструкцій [Установка модулей PECL](install.pecl.md). Виконайте команду **configure** вказавши місцезнаходження заголовкових файлів та бібліотек Informix Client SDK:

```
bash$ ./configure --with-pdo-informix=/path/to/SDK[,shared]
```

За замовчуванням команда **configure** буде використовувати значення змінної оточення `INFORMIXDIR`

## Перемотується курсор

PDOINFORMIX підтримує курсори, що перемотуються; проте за умовчанням їх використання не дозволено. Для дозволу їхньої підтримки ви повинні вказати **`ENABLESCROLLABLECURSORS=1`** у відповідних налаштуваннях з'єднання ODBC в odbc.ini або встановити параметр **`EnableScrollableCursors=1`** у рядку з'єднання (DSN).

## Зміст

-   [PDOINFORMIX DSN](ref.pdo-informix.connection.md) — З'єднання з базою даних Informix
