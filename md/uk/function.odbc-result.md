---
navigation:
  - function.odbc-result-all.md: « odbc\_result\_all
  - function.odbc-rollback.md: odbc\_rollback »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_result

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_result — Отримує дані результату

### Опис

```methodsynopsis
odbc_result(resource $statement, string|int $field): string|bool|null
```

Отримує дані результату.

### Список параметрів

`statement`

Ресурс ODBC.

`field`

Ім'я поля. Це може бути ціле число, що містить номер шпальти потрібного поля; або це може бути рядок, який містить ім'я поля.

### Значення, що повертаються

Повертає рядковий вміст поля, **`false`**в случае возникновения ошибки,**`null`** для даних NULL або **`true`** для бінарних даних.

### Приклади

Перший виклик **odbc\_result()** повертає значення третього поля у поточному записі результату запиту. Другий виклик функції **odbc\_result()** повертає значення поля з ім'ям "val" у поточному записі результату запиту. Помилка виникає, якщо параметр номера стовпця для поля менше одиниці або перевищує кількість стовпців (або полів) у поточному записі. Також помилка виникає при спробі отримання стовпця з ім'ям, яке не є одним з імен полів таблиці, що запитується (або декількох таблиць).

**Приклад #1 Приклади використання **odbc\_result()****

```php
<?php
$item_3   = odbc_result($Query_ID, 3);
$item_val = odbc_result($Query_ID, "val");
?>
```

### Примітки

Індекси полів починаються з 1. Для отримання інформації про спосіб повернення двійкових даних або даних стовпців LONG необхідно звернутися до [odbc\_binmode()](function.odbc-binmode.md) і [odbc\_longreadlen()](function.odbc-longreadlen.md)
