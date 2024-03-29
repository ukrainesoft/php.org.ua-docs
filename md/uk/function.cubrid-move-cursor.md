---
navigation:
  - function.cubrid-lock-write.md: « cubrid\_lock\_write
  - function.cubrid-next-result.md: cubrid\_next\_result »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_move\_cursor
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_move\_cursor

(PECL CUBRID >= 8.3.0)

cubrid\_move\_cursor — Переміщує курсор у результаті

### Опис

```methodsynopsis
cubrid_move_cursor(resource $req_identifier, int $offset, int $origin = CUBRID_CURSOR_CURRENT): bool
```

Функция**cubrid\_move\_cursor()** використовується для переміщення поточного положення курсору `req_identifier`на значение, заданное в аргументе`offset`, в направлении, заданном в аргументе`origin`. Щоб встановити аргумент `origin`, Ви можете використовувати \*\*`CUBRID_CURSOR_FIRST`**для первой части результата,**`CUBRID_CURSOR_CURRENT`**для текущего местоположения результата или**`CUBRID_CURSOR_LAST`**для последней части результата. Если аргумент`origin`не указан явно, тогда функция использует**`CUBRID_CURSOR_CURRENT`\*\*в качестве значения по умолчанию.

Якщо значення діапазону переміщення курсору перевищує допустиму межу, то курсор переміщається в наступне місце після допустимого діапазону курсору. Наприклад, якщо ви перемістите 20 одиниць в результаті розміром 10, то курсор переміститься на 11-е місце і поверне **`CUBRID_NO_MORE_DATA`**

### Список параметрів

`req_identifier`

Ідентифікатор запиту.

`offset`

Кількість одиниць, куди потрібно перемістити курсор.

`origin`

Місце, з якого ви бажаєте перемістити курсор: **`CUBRID_CURSOR_FIRST`** **`CUBRID_CURSOR_CURRENT`** або **`CUBRID_CURSOR_LAST`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_move\_cursor()\*\*\*\*

```php
<?php
$conn = cubrid_connect("127.0.0.1", 33000, "demodb", "dba");

$req = cubrid_execute($conn, "SELECT * FROM code");
cubrid_move_cursor($req, 1, CUBRID_CURSOR_LAST);

$result = cubrid_fetch_row($req);
var_dump($result);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$result = cubrid_fetch_row($req);
var_dump($result);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_CURRENT);
$result = cubrid_fetch_row($req);
var_dump($result);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

```
array(2) {
  [0]=>
  string(1) "G"
  [1]=>
  string(4) "Gold"
}
array(2) {
  [0]=>
  string(1) "X"
  [1]=>
  string(5) "Mixed"
}
array(2) {
  [0]=>
  string(1) "M"
  [1]=>
  string(3) "Man"
}
```

### Дивіться також

-   [cubrid\_execute()](function.cubrid-execute.md) \- Виконує підготовлений SQL-оператор
