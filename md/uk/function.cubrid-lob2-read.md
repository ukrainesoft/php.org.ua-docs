---
navigation:
  - function.cubrid-lob2-new.html: « cubridlob2new
  - function.cubrid-lob2-seek64.html: cubridlob2seek64 »
  - index.md: PHP Manual
  - ref.cubrid.md: Функции CUBRID
title: cubridlob2read
---
# cubridlob2read

(PECL CUBRID >= 8.4.1)

cubridlob2read — Здійснює читання з даних BLOB/CLOB

### Опис

```methodsynopsis
cubrid_lob2_read(resource $lob_identifier, int $len): string
```

Функція **cubridlob2read()** зчитує `len` байтів із даних LOB і повертає прочитані байти.

### Список параметрів

`lob_identifier`

Ідентифікатор LOB, повернутий функцією [cubridlob2new()](function.cubrid-lob2-new.md) або отриманий із результуючого набору.

`len`

Довжина буфера, що використовується для читання з даних LOB.

### Значення, що повертаються

Повертає вміст у вигляді рядка, \*\*`false`\*\*якщо даних більше немає, або **`null`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridlob2read()****

```php
<?php
// test_lob (id INT, contents CLOB)

$conn = cubrid_connect("localhost", 33000, "demodb", "public", "");

$req = cubrid_execute($conn, "select * from test_lob");

$row = cubrid_fetch_row($req, CUBRID_LOB);

print "текущая позиция - " . cubrid_lob2_tell($row[1]) . "\n";

cubrid_lob2_seek($row[1], 10, CUBRID_CURSOR_FIRST);

print "\nпозиция после движения вперед - " . cubrid_lob2_tell($row[1]) . "\n";

$data = cubrid_lob2_read($row[1], 12);

print "\nпозиция после чтения - " . cubrid_lob2_tell($row[1]) . "\n";

print $data . "\n";

cubrid_lob2_seek($row[1], 5, CUBRID_CURSOR_CURRENT);

print "\nпозиция после повторного движения вперед - " . cubrid_lob2_tell($row[1]) . "\n";

$data = cubrid_lob2_read($row[1], 20);
print $data . "\n";

cubrid_disconnect($conn);
?>
```

**Приклад #2 Приклад використання **cubridlob2read()****

```php
<?php
// test_lob (id INT, contents CLOB)

$conn = cubrid_connect("localhost", 33000, "demodb", "dba", "");

$req = cubrid_execute($conn, "select * from test_lob");

$row = cubrid_fetch_row($req, CUBRID_LOB);

while (true) {
    if ($data = cubrid_lob2_read($row[1], 1024)) {
        print $data . "\n";
    }
    elseif ($data === false) {
        print "Данных больше нет\n";
        break;
    }
    else {
        print "Произошла ошибка\n";
        break;
    }
}

cubrid_disconnect($conn);
?>
```

### Дивіться також

-   [cubridlob2write()](function.cubrid-lob2-write.md) - Записує до LOB-об'єкту
-   [cubridlob2seek()](function.cubrid-lob2-seek.md) - Переміщує курсор LOB-об'єкта
-   [cubridlob2seek64()](function.cubrid-lob2-seek64.md) - Переміщує курсор LOB-об'єкта
-   [cubridlob2tell()](function.cubrid-lob2-tell.md) - Повідомляє положення курсору LOB-об'єкта
-   [cubridlob2tell64()](function.cubrid-lob2-tell64.md) - Повідомляє положення курсору LOB-об'єкта
-   [cubridlob2size()](function.cubrid-lob2-size.md) - Отримує розмір LOB-об'єкта
-   [cubridlob2size64()](function.cubrid-lob2-size64.md) - Отримує розмір LOB-об'єкта
