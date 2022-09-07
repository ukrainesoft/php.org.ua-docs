---
navigation:
  - function.dba-handlers.md: « dbahandlers
  - function.dba-key-split.md: dbakeysplit »
  - index.md: PHP Manual
  - ref.dba.md: Функції DBA
title: dbainsert
---
# dbainsert

(PHP 4, PHP 5, PHP 7, PHP 8)

dbainsert — Вставляє запис

### Опис

```methodsynopsis
dba_insert(string|array $key, string $value, resource $dba): bool
```

**dbainsert()** вставляє до бази даних запис заданий параметрами `key` і `value`

### Список параметрів

`key`

Ключ запису для вставки. Якщо такий ключ вже існує у базі даних, функція завершиться з помилкою. Для заміни запису використовуйте функцію [dbareplace()](function.dba-replace.md)

`value`

Значення для вставки.

`dba`

Обробник бази даних, повернутий [dbaopen()](function.dba-open.md) або [dbapopen()](function.dba-popen.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [dbaexists()](function.dba-exists.md) - Перевіряє, чи існує ключ
-   [dbadelete()](function.dba-delete.md) - Видаляє запис бази даних, визначену ключем
-   [dbafetch()](function.dba-fetch.md) - Витягує дані за вказаним ключем
-   [dbareplace()](function.dba-replace.md) - Перезаписати або вставити запис
