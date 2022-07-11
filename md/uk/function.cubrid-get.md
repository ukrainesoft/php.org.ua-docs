- [«cubrid_get_server_info](function.cubrid-get-server-info.md)
- [cubrid_insert_id »](function.cubrid-insert-id.md)

- [PHP Manual](index.md)
- [Функції CUBRID](ref.cubrid.md)
- Отримує стовпець, використовуючи OID

#cubrid_get

(PECL CUBRID = 8.3.0)

cubrid_get — Отримує стовпець, використовуючи OID

### Опис

**cubrid_get**(resource `$conn_identifier`, string `$oid`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$attr` = ?):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

Функція **cubrid_get()** використовується для отримання атрибута екземпляра
цього `oid`. Ви можете отримати один атрибут, використовуючи рядковий тип
даних для аргументу `attr`, або багато атрибутів, використовуючи тип
даних масиву для аргументу `attr`.

### Список параметрів

`conn_identifier`
Ідентифікатор з'єднання.

`oid`
OID екземпляра, який ви хочете прочитати.

`attr`
Назва атрибута, який ви хочете прочитати.

### Значення, що повертаються

вміст запитаного атрибуту, коли процес успішний; Коли `attr`
встановлений з рядковим типом даних, результат повертається як
рядки; якщо для `attr` заданий тип даних масиву (числовий масив,
що починається з 0), результат повертається в асоціативному масиві.
Коли `attr` опущений, всі атрибути приймаються як масиву.

**`false`**, якщо процес завершився з помилкою або результат NULL (якщо
виникає помилка, щоб відрізнити порожній рядок від NULL, друкується
попереджувальне повідомлення. Ви можете перевірити помилку, використовуючи
[cubrid_error_code()](function.cubrid-error-code.md))

### Приклади

**Приклад #1 Приклад використання **cubrid_get()****

` <?php$conn = cubrid_connect("localhost", 33000, "demodb");@cubrid_execute($conn, "DROP TABLE foo");cubrid_execute($conn, "CREATE TABLE foo  int), c list(int), d char(10))");cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(1, {1,2,3}, {11) ,22,33,333}, 'a')");cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(2, {4,5,7}, {44,55,66,666} , 'b')");$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST$cu| $conn, $oid, "b");var_dump($attr);$attr = cubrid_get($conn, $oid);var_dump($attr);cubrid_close_request($req);cubrid_disconnect($conn);?> `

Результат виконання цього прикладу:

string(9) "{1, 2, 3}"
array(4) {
["a"]=>
string(1) "1"
["b"]=>
array(3) {
[0]=>
string(1) "1"
[1]=>
string(1) "2"
[2]=>
string(1) "3"
}
["c"]=>
array(4) {
[0]=>
string(2) "11"
[1]=>
string(2) "22"
[2]=>
string(2) "33"
[3]=>
string(3) "333"
}
["d"]=>
string(10) "a"
}

### Дивіться також

- [cubrid_put()](function.cubrid-put.md) - Оновлює стовпець з
використанням OID
