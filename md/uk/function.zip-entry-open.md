---
navigation:
  - function.zip-entry-name.md: « zipentryname
  - function.zip-entry-read.md: zipentryread »
  - index.md: PHP Manual
  - ref.zip.md: Функции Zip
title: zipentryopen
---
# zipentryopen

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zipentryopen — Відкриває директорію для читання

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
zip_entry_open(resource $zip_dp, resource $zip_entry, string $mode = "rb"): bool
```

Відкриває директорію у ZIP-архіві для читання.

### Список параметрів

`zip_dp`

Дескриптор, що повертається функцією [zipopen()](function.zip-open.md)

`zip_entry`

Дескриптор директорії, що повертається функцією [zipread()](function.zip-read.md)

`mode`

Доступні режими наведено у документації до функції [fopen()](function.fopen.md)

> **Зауваження**
> 
> В даний час параметр `mode` ігнорується і завжди має значення `"rb"`. Це з тим, що ZIP в PHP підтримується лише у режимі читання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

> **Зауваження**
> 
> На відміну від функції [fopen()](function.fopen.md) та інших подібних функцій, значення, що повертається функцією **zipentryopen()** тільки інформує нас про результат виконання операції та не потрібно для подальшого читання чи закриття дескриптора директорії.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція застаріла на користь Object API. |

### Дивіться також

-   [zipentryclose()](function.zip-entry-close.md) - закриває дескриптор директорії
-   [zipentryread()](function.zip-entry-read.md) - Читає дані із відкритого раніше дескриптора директорії
