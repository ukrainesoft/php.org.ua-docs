---
navigation:
  - function.dba-close.md: « dba\_close
  - function.dba-exists.md: dba\_exists »
  - index.md: PHP Manual
  - ref.dba.md: Функції DBA
title: dba\_delete
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dba\_delete

(PHP 4, PHP 5, PHP 7, PHP 8)

dba\_delete — Видалення запису бази даних, визначеної ключем.

### Опис

```methodsynopsis
dba_delete(string|array $key, resource $dba): bool
```

**dba\_delete()** видаляє вказаний запис у базі даних.

### Список параметрів

`key`

Ключ запису, який потрібно видалити.

`dba`

Обробник бази даних, повернутий [dba\_open()](function.dba-open.md) або [dba\_popen()](function.dba-popen.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [dba\_exists()](function.dba-exists.md) \- Перевіряє, чи існує ключ
-   [dba\_fetch()](function.dba-fetch.md) \- Витягує дані за вказаним ключем
-   [dba\_insert()](function.dba-insert.md) \- Вставляє запис
-   [dba\_replace()](function.dba-replace.md) \- Перезаписати або вставити запис
