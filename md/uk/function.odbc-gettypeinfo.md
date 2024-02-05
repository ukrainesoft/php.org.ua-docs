---
navigation:
  - function.odbc-free-result.md: « odbc\_free\_result
  - function.odbc-longreadlen.md: odbc\_longreadlen »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_gettypeinfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_gettypeinfo

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_gettypeinfo — Повертає інформацію про типи даних, що підтримуються джерелом даних

### Опис

```methodsynopsis
odbc_gettypeinfo(resource $odbc, int $data_type = 0): resource|false
```

Повертає інформацію про типи даних, що підтримуються джерелом даних.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbc\_connect()](function.odbc-connect.md)

`data_type`

Тип даних, який можна використовуватиме обмеження інформації до одного типу даних.

### Значення, що повертаються

Повертає ідентифікатор результату ODBC або \*\*`false`\*\*в случае возникновения ошибки.

У результуючому наборі є такі стовпці:

-   TYPE\_NAME
-   DATA\_TYPE
-   PRECISION
-   LITERAL\_PREFIX
-   LITERAL\_SUFFIX
-   CREATE\_PARAMS
-   NULLABLE
-   CASE\_SENSITIVE
-   SEARCHABLE
-   UNSIGNED\_ATTRIBUTE
-   MONEY
-   AUTO\_INCREMENT
-   LOCAL\_TYPE\_NAME
-   MINIMUM\_SCALE
-   MAXIMUM\_SCALE

Набір результатів упорядкований за DATA\_TYPE та TYPE\_NAME.
