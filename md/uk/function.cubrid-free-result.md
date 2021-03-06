- [«cubrid_fetch](function.cubrid-fetch.md)
- [cubrid_get_autocommit »](function.cubrid-get-autocommit.md)

- [PHP Manual](index.md)
- [Функції CUBRID](ref.cubrid.md)
- звільняє пам'ять, зайняту даними результату

#cubrid_free_result

(PECL CUBRID = 8.3.0)

cubrid_free_result — Звільняє пам'ять, зайняту даними результату

### Опис

**cubrid_free_result**(resource `$req_identifier`): bool

Функція звільняє пам'ять, зайняту даними результату. Вона повертає
**`true`** у разі успішного виконання або **`false`** у разі
виникнення помилки. Варто звернути увагу на те, що функція тепер може
тільки звільняти буфер вибірки клієнта, і якщо необхідно звільнити
усю пам'ять, то потрібно використовувати функцію
[cubrid_close_request()](function.cubrid-close-request.md).

### Список параметрів

`req_identifier`
Ідентифікатор запиту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubrid_free_result()****

` <?php$conn = cubrid_connect("localhost", 33000, "demodb");$req = cubrid_execute($conn, "SELECT * FROM history WHERE host_year=2004  );var_dump($row);cubrid_free_result($req);cubrid_close_request($req);cubrid_disconnect($conn);?> `

Результат виконання цього прикладу:

array(5) {
["event_code"]=>
string(5) "20005"
["athlete"]=>
string(12) "Hayes Joanna"
["host_year"]=>
string(4) "2004"
["score"]=>
string(5) "12.37"
["unit"]=>
string(4) "time"
}
