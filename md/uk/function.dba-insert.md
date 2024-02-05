---
navigation:
  - function.dba-handlers.md: « dba\_handlers
  - function.dba-key-split.md: dba\_key\_split »
  - index.md: PHP Manual
  - ref.dba.md: Функції DBA
title: dba\_insert
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dba\_insert

(PHP 4, PHP 5, PHP 7, PHP 8)

dba\_insert — Вставляє запис

### Опис

```methodsynopsis
dba_insert(string|array $key, string $value, resource $dba): bool
```

**dba\_insert()** вставляє в базу даних запис заданий параметрами `key`и`value`

### Список параметрів

`key`

Ключ запису для вставки. Якщо такий ключ вже існує у базі даних, функція завершиться з помилкою. Для заміни запису використовуйте функцію [dba\_replace()](function.dba-replace.md)

`value`

Значення для вставки.

`dba`

Обробник бази даних, повернутий [dba\_open()](function.dba-open.md) або [dba\_popen()](function.dba-popen.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [dba\_exists()](function.dba-exists.md) \- Перевіряє, чи існує ключ
-   [dba\_delete()](function.dba-delete.md) \- Видаляє запис бази даних, визначену ключем
-   [dba\_fetch()](function.dba-fetch.md) \- Витягує дані за вказаним ключем
-   [dba\_replace()](function.dba-replace.md) \- Перезаписати або вставити запис
