---
navigation:
  - function.pg-fetch-all.md: « pgfetchall
  - function.pg-fetch-assoc.md: пгfetchassoc »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгfetcharray
---
# пгfetcharray

(PHP 4, PHP 5, PHP 7, PHP 8)

пгfetcharray — Повертає рядок результату у вигляді масиву

### Опис

```methodsynopsis
pg_fetch_array(PgSql\Result $result, ?int $row = null, int $mode = PGSQL_BOTH): array|false
```

**пгfetcharray()** повертає масив, що відповідає обраному рядку (запису).

**пгfetcharray()** розширена версія функції [пгfetchrow()](function.pg-fetch-row.md). Ця функція здатна зберегти дані не лише з цифровими індексами, а й з асоціативними (ім'я поля). За умовчанням зберігає і ті, й інші.

> **Зауваження**: Ця функція встановлює NULL-поля значення **`null`** PHP.

**пгfetcharray()** виконується трохи повільніше ніж [пгfetchrow()](function.pg-fetch-row.md)але значно простіше у використанні.

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.md), що повертається функціями [пгquery()](function.pg-query.md) [пгqueryparams()](function.pg-query-params.md) або [пгexecute()](function.pg-execute.md) (між іншим).

`row`

Номер рядка в результат для вибірки. Рядки пронумеровані з 0 за зростанням. Якщо параметр опущено або передано **`null`** буде вибрано наступний рядок.

`mode`

Необов'язковий параметр, керуючий тим, як індексується масив, що повертається (array). Параметр `mode` є константою і може приймати такі значення: **`PGSQL_ASSOC`** **`PGSQL_NUM`** і **`PGSQL_BOTH`**. При використанні **`PGSQL_NUM`** функція повертає масив із числовими індексами, при використанні **`PGSQL_ASSOC`** вона поверне лише асоціативні індекси, а **`PGSQL_BOTH`** поверне як числові, і асоціативні індекси.

### Значення, що повертаються

Масив (array) з числовими індексами (починаючи з 0), або асоціативними (на ім'я поля), або з обома типами індексів. Кожне значення у масиві (array) представлено як рядок (string). Значення `NULL` повертається як **`null`**

Функція повертає **`false`**, якщо `row` виходить за рамки кількості рядків у вибірці, чи відсутності рядків, чи у разі будь-якої іншої помилки. Вибірка з результату запиту, відмінного від SELECT, також поверне **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгfetcharray()****

```php
<?php

$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
  echo "Произошла ошибка.\n";
  exit;
}

$result = pg_query($conn, "SELECT author, email FROM authors");
if (!$result) {
  echo "Произошла ошибка.\n";
  exit;
}

$arr = pg_fetch_array($result, 0, PGSQL_NUM);
echo $arr[0] . " <- Row 1 Author\n";
echo $arr[1] . " <- Row 1 E-mail\n";

// Параметр row необязателен,
// для передечи result_type вместо row можно передать NULL.
// Успешные вызовы pg_fetch_array вернут следующий ряд.

$arr = pg_fetch_array($result, NULL, PGSQL_ASSOC);
echo $arr["author"] . " <- Row 2 Author\n";
echo $arr["email"] . " <- Row 2 E-mail\n";

$arr = pg_fetch_array($result);
echo $arr["author"] . " <- Row 3 Author\n";
echo $arr[1] . " <- Row 3 E-mail\n";

?>
```

### Дивіться також

-   [пгfetchrow()](function.pg-fetch-row.md) - Вибирає рядок результату запиту та поміщає дані до масиву
-   [пгfetchobject()](function.pg-fetch-object.md) - Вибирає рядок результату запиту та повертає дані у вигляді об'єкта
-   [пгfetchresult()](function.pg-fetch-result.md) - Повертає запис із результату запиту
