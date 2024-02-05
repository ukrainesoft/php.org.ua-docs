---
navigation:
  - function.dba-popen.md: « dba\_popen
  - function.dba-sync.md: dba\_sync »
  - index.md: PHP Manual
  - ref.dba.md: Функції DBA
title: dba\_replace
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dba\_replace

(PHP 4, PHP 5, PHP 7, PHP 8)

dba\_replace — Перезаписати або вставити запис

### Опис

```methodsynopsis
dba_replace(string|array $key, string $value, resource $dba): bool
```

**dba\_replace()** перезаписує або вставляє запис, заданий ключем `key`и значением`value` до бази даних, визначеної обробником `dba`

### Список параметрів

`key`

Ключ запису, який потрібно замінити.

`value`

Нове значення.

`dba`

Обробник бази даних, повернутий [dba\_open()](function.dba-open.md) або [dba\_popen()](function.dba-popen.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [dba\_exists()](function.dba-exists.md) \- Перевіряє, чи існує ключ
-   [dba\_delete()](function.dba-delete.md) \- Видаляє запис бази даних, визначену ключем
-   [dba\_fetch()](function.dba-fetch.md) \- Витягує дані за вказаним ключем
-   [dba\_insert()](function.dba-insert.md) \- Вставляє запис
