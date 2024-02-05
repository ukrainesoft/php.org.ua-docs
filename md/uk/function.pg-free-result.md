---
navigation:
  - function.pg-flush.md: « pg\_flush
  - function.pg-get-notify.md: pg\_get\_notify »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_free\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_free\_result

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_free\_result — Очищення результату запиту та звільнення пам'яті

### Опис

```methodsynopsis
pg_free_result(PgSql\Result $result): bool
```

**pg\_free\_result()** звільняє пам'ять, зайняту екземпляром [PgSql\\Result](class.pgsql-result.md)

Викликати цю функцію слід лише у разі нестачі пам'яті під час виконання скрипту. У будь-якому випадку пам'ять буде звільнено автоматично після закінчення роботи скрипту.

> **Зауваження** :
> 
> Прежнее название функции:**pg\_freeresult()**

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_free\_result()\*\*\*\*

```php
<?php
$db = pg_connect("dbname=users user=me") || die();

$res = pg_query($db, "SELECT 1 UNION ALL SELECT 2");

$val = pg_fetch_result($res, 1, 0);

echo "Первое поле во второй строчке: ", $val, "\n";

pg_free_result($res);
?>
```

Результат виконання наведеного прикладу:

```
Первое поле во второй строчке: 2
```

### Дивіться також

-   [pg\_query()](function.pg-query.md) \- Виконує запит
-   [pg\_query\_params()](function.pg-query-params.md) \- Надсилає параметризований запит на сервер, параметри передаються окремо від тексту SQL запиту
-   [pg\_execute()](function.pg-execute.md) \- Запускає виконання раніше підготовленого параметризованого запиту та чекає результату
