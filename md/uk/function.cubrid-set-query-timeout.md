---
navigation:
  - function.cubrid-set-drop.md: « cubrid\_set\_drop
  - function.cubrid-version.md: cubrid\_version »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_set\_query\_timeout
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_set\_query\_timeout

(PECL CUBRID >= 8.4.1)

cubrid\_set\_query\_timeout — Встановлює час очікування на виконання запиту

### Опис

```methodsynopsis
cubrid_set_query_timeout(resource $req_identifier, int $timeout): bool
```

Функция**cubrid\_set\_query\_timeout()** використовується для встановлення часу очікування на виконання запиту.

### Список параметрів

`req_identifier`

Request identifier.

`timeout`

Час очікування в мілісекундах.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [cubrid\_get\_query\_timeout()](function.cubrid-get-query-timeout.md) \- Отримує значення часу очікування запиту
