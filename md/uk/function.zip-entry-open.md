---
navigation:
  - function.zip-entry-name.md: « zip\_entry\_name
  - function.zip-entry-read.md: zip\_entry\_read »
  - index.md: PHP Manual
  - ref.zip.md: Функції Zip
title: zip\_entry\_open
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# zip\_entry\_open

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zip\_entry\_open — Відкриває директорію для читання

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
zip_entry_open(resource $zip_dp, resource $zip_entry, string $mode = "rb"): bool
```

Відкриває директорію у ZIP-архіві для читання.

### Список параметрів

`zip_dp`

Дескриптор, що повертається функцією [zip\_open()](function.zip-open.md)

`zip_entry`

Дескриптор директорії, що повертається функцією [zip\_read()](function.zip-read.md)

`mode`

Доступні режими наведено у документації до функції [fopen()](function.fopen.md)

> **Зауваження** :
> 
> В настоящее время параметр`mode` ігнорується і завжди має значення `"rb"`. Це з тим, що ZIP в PHP підтримується лише у режимі читання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

> **Зауваження** :
> 
> В отличие от функции[fopen()](function.fopen.md) та інших подібних функцій, значення, що повертається функцією **zip\_entry\_open()** тільки інформує нас про результат виконання операції та не потрібно для подальшого читання чи закриття дескриптора директорії.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція застаріла на користь Object API. |

### Дивіться також

-   [zip\_entry\_close()](function.zip-entry-close.md) \- закриває дескриптор директорії
-   [zip\_entry\_read()](function.zip-entry-read.md) \- Читає дані із відкритого раніше дескриптора директорії
