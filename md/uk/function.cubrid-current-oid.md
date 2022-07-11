- [«cubrid_connect](function.cubrid-connect.md)
- [cubrid_disconnect »](function.cubrid-disconnect.md)

- [PHP Manual](index.md)
- [Функції CUBRID](ref.cubrid.md)
- Повертає OID поточної позиції курсору

#cubrid_current_oid

(PECL CUBRID = 8.3.0)

cubrid_current_oid — Повертає OID поточної позиції курсору

### Опис

**cubrid_current_oid**(resource `$req_identifier`): string

Функція **cubrid_current_oid()** використовується для отримання поточного oid
положення курсору в результативному наборі. Для використання функції
**cubrid_current_oid()**, запущений запит має бути оновлюваним, та
при запуску запиту було встановлено опцію **`CUBRID_INCLUDE_OID`**.

### Список параметрів

`req_identifier`
Ідентифікатор запиту.

### Значення, що повертаються

Oid поточного положення курсору, у разі успішного виконання або
**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubrid_current_oid()****

` <?php$conn==cubrid_connect("localhost", 33000, "demodb", "dba");$req = cubrid_execute($conn, "SELECT **FROM code", CUBRID_INCLU ;$res = cubrid_get($conn, $oid);print_r($res);cubrid_disconnect($conn);?> `

Результат виконання цього прикладу:

Array
(
[s_name] => X
[f_name] => mixed
)

### Дивіться також

- [cubrid_execute()](function.cubrid-execute.md) - Виконує
підготовлений SQL-оператор
