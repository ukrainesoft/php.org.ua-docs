---
navigation:
  - function.pg-fetch-all.md: « pg\_fetch\_all
  - function.pg-fetch-assoc.md: pg\_fetch\_assoc »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_fetch\_array
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_fetch\_array

(PHP 4, PHP 5, PHP 7, PHP 8)

pg\_fetch\_array — Повертає рядок результату у вигляді масиву

### Опис

```methodsynopsis
pg_fetch_array(PgSql\Result $result, ?int $row = null, int $mode = PGSQL_BOTH): array|false
```

**pg\_fetch\_array()** повертає масив, що відповідає обраному рядку (запису).

**pg\_fetch\_array()** розширена версія функції [pg\_fetch\_row()](function.pg-fetch-row.md). Ця функція здатна зберегти дані не лише з цифровими індексами, а й з асоціативними (ім'я поля). За умовчанням зберігає і ті, й інші.

> **Зауваження**: Ця функція встановлює NULL-поля значення \*\*`null`\*\*PHP.

**pg\_fetch\_array()** виконується трохи повільніше ніж [pg\_fetch\_row()](function.pg-fetch-row.md)але значно простіше у використанні.

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

`row`

Номер рядка в результат для вибірки. Рядки пронумеровані з 0 за зростанням. Якщо параметр опущено або передано **`null`** буде вибрано наступний рядок.

`mode`

Необов'язковий параметр, керуючий тим, як індексується масив, що повертається (array). Параметр `mode` є константою і може приймати такі значення: **`PGSQL_ASSOC`** **`PGSQL_NUM`**и**`PGSQL_BOTH`**При использовании**`PGSQL_NUM`** функція повертає масив із числовими індексами, при використанні **`PGSQL_ASSOC`** вона поверне лише асоціативні індекси, а **`PGSQL_BOTH`** поверне як числові, і асоціативні індекси.

### Значення, що повертаються

Масив (array) з числовими індексами (починаючи з 0), або асоціативними (на ім'я поля), або з обома типами індексів. Кожне значення у масиві (array) представлено як рядок (string). Значення `NULL` повертається як **`null`**

Функція повертає **`false`**, якщо `row` виходить за рамки кількості рядків у вибірці, чи відсутності рядків, чи у разі будь-якої іншої помилки. Вибірка з результату запиту, відмінного від SELECT, також поверне **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_fetch\_array()\*\*\*\*

```php
<?php

$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
  echo "Произошла ошибка.\n";
  exit;
}

$result = pg_query($conn, "SELECT author, email FROM authors");
if (!$result) {
  echo "Произошла ошибка.\n";
  exit;
}

$arr = pg_fetch_array($result, 0, PGSQL_NUM);
echo $arr[0] . " <- Row 1 Author\n";
echo $arr[1] . " <- Row 1 E-mail\n";

// Параметр row необязателен,
// для передечи result_type вместо row можно передать NULL.
// Успешные вызовы pg_fetch_array вернут следующий ряд.

$arr = pg_fetch_array($result, NULL, PGSQL_ASSOC);
echo $arr["author"] . " <- Row 2 Author\n";
echo $arr["email"] . " <- Row 2 E-mail\n";

$arr = pg_fetch_array($result);
echo $arr["author"] . " <- Row 3 Author\n";
echo $arr[1] . " <- Row 3 E-mail\n";

?>
```

### Дивіться також

-   [pg\_fetch\_row()](function.pg-fetch-row.md) \- Вибирає рядок результату запиту та поміщає дані до масиву
-   [pg\_fetch\_object()](function.pg-fetch-object.md) \- Вибирає рядок результату запиту та повертає дані у вигляді об'єкта
-   [pg\_fetch\_result()](function.pg-fetch-result.md) \- Повертає запис із результату запиту
