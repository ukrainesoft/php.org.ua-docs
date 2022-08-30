Переміщує курсор у результаті

-   [« cubridlockwrite](function.cubrid-lock-write.html)
    
-   [cubridnextresult »](function.cubrid-next-result.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Переміщує курсор у результаті
    

# cubridmovecursor

(PECL CUBRID >= 8.3.0)

cubridmovecursor — Переміщує курсор у результаті

### Опис

```methodsynopsis
cubrid_move_cursor(resource $req_identifier, int $offset, int $origin = CUBRID_CURSOR_CURRENT): bool
```

Функція **cubridmovecursor()** використовується для переміщення поточного положення курсору `req_identifier` значення, задане в аргументі `offset`, у напрямку, заданому в аргументі `origin`. Щоб встановити аргумент `origin`, Ви можете використовувати **`CUBRID_CURSOR_FIRST`** для першої частини результату, **`CUBRID_CURSOR_CURRENT`** для поточного розташування результату або **`CUBRID_CURSOR_LAST`** для останньої частини результату. Якщо аргумент `origin` не вказано явно, тоді функція використовує **`CUBRID_CURSOR_CURRENT`** як значення за замовчуванням.

Якщо значення діапазону переміщення курсору перевищує допустиму межу, то курсор переміщається в наступне місце після допустимого діапазону курсору. Наприклад, якщо ви перемістите 20 одиниць в результаті розміром 10, то курсор переміститься на 11-е місце і поверне **`CUBRID_NO_MORE_DATA`**

### Список параметрів

`req_identifier`

Ідентифікатор запиту.

`offset`

Кількість одиниць, куди потрібно перемістити курсор.

`origin`

Місце, з якого ви бажаєте перемістити курсор: **`CUBRID_CURSOR_FIRST`** **`CUBRID_CURSOR_CURRENT`** або **`CUBRID_CURSOR_LAST`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridmovecursor()****

```php
<?php
$conn = cubrid_connect("127.0.0.1", 33000, "demodb", "dba");

$req = cubrid_execute($conn, "SELECT * FROM code");
cubrid_move_cursor($req, 1, CUBRID_CURSOR_LAST);

$result = cubrid_fetch_row($req);
var_dump($result);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$result = cubrid_fetch_row($req);
var_dump($result);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_CURRENT);
$result = cubrid_fetch_row($req);
var_dump($result);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

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

-   [cubridexecute()](function.cubrid-execute.html) - Виконує підготовлений SQL-оператор