Повертає ідентифікатор, згенерований для останнього оновленого стовпця AUTOINCREMENT

-   [« cubridget](function.cubrid-get.html)
    
-   [cubridісinstance »](function.cubrid-is-instance.html)
    
-   [PHP Manual](index.md)
    
-   [Функции CUBRID](ref.cubrid.md)
    
-   Повертає ідентифікатор, згенерований для останнього оновленого стовпця AUTOINCREMENT
    

# cubridinsertід

(PECL CUBRID >= 8.3.0)

cubridinsertid — Повертає ідентифікатор, згенерований для останнього оновленого стовпця **`AUTO_INCREMENT`**

### Опис

```methodsynopsis
cubrid_insert_id(resource $conn_identifier = ?): string
```

Функція **cubridinsertid()** повертає ідентифікатор, згенерований для стовпця AUTOINCREMENT, що оновлюється попереднім запитом INSERT. Вона повертає 0, якщо попередній запит не генерує нові рядки, або FALSE у разі помилки.

> **Зауваження**
> 
> CUBRID підтримує AUTOINCREMENT для більш ніж одного шпальти в таблиці. У більшості випадків у таблиці буде один стовпець AUTOINCREMENT. Якщо є кілька стовпців AUTOINCREMENT, цю функцію не слід використовувати, навіть якщо вона поверне значення.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання, отриманий раніше під час виклику [cubridconnect()](function.cubrid-connect.html)

### Значення, що повертаються

Рядок, що представляє ідентифікатор, згенерований для стовпця AUTOINCREMENT попереднім запитом у разі успішного виконання.

0 якщо попередній запит не згенерував нові рядки.

**`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Значення, що повертається у вигляді масиву замінено на рядок; Видалено перший параметр classname. |

### Приклади

**Приклад #1 Приклад використання **cubridinsertid()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

@cubrid_execute($conn, "DROP TABLE cubrid_test");
cubrid_execute($conn, "CREATE TABLE cubrid_test (d int AUTO_INCREMENT(1, 2), t varchar)");

for ($i = 0; $i < 10; $i++) {
    cubrid_execute($conn, "INSERT INTO cubrid_test(t) VALUES('cubrid_test')");
}

$id = cubrid_insert_id();
var_dump($id);

cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
string(2) "19"
```