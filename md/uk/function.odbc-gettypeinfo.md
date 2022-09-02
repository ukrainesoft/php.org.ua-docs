---
navigation:
  - function.odbc-free-result.md: « odbcfreeresult
  - function.odbc-longreadlen.md: odbclongreadlen »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbcgettypeinfo
---
# odbcgettypeinfo

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcgettypeinfo — Повертає інформацію про типи даних, що підтримуються джерелом даних

### Опис

```methodsynopsis
odbc_gettypeinfo(resource $odbc, int $data_type = 0): resource|false
```

Повертає інформацію про типи даних, що підтримуються джерелом даних.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, див. [odbcconnect()](function.odbc-connect.md)

`data_type`

Тип даних, який можна використовуватиме обмеження інформації до одного типу даних.

### Значення, що повертаються

Повертає ідентифікатор результату ODBC або **`false`** у разі виникнення помилки.

У результуючому наборі є такі стовпці:

-   TYPENAME
-   DATATYPE
-   PRECISION
-   LITERALPREFIX
-   LITERALSUFFIX
-   CREATEPARAMS
-   NULLABLE
-   CASESENSITIVE
-   SEARCHABLE
-   UNSIGNEDATTRIBUTE
-   MONEY
-   AUTOINCREMENT
-   LOCALTYPENAME
-   MINIMUMSCALE
-   MAXIMUMSCALE

Набір результатів упорядкований за DATATYPE та TYPENAME.
