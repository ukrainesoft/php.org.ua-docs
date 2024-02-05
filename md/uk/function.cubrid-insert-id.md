---
navigation:
  - function.cubrid-get.md: « cubrid\_get
  - function.cubrid-is-instance.md: cubrid\_is\_instance »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_insert\_id
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_insert\_id

(PECL CUBRID >= 8.3.0)

cubrid\_insert\_id — Повертає ідентифікатор, згенерований для останнього оновленого стовпця **`AUTO_INCREMENT`**

### Опис

```methodsynopsis
cubrid_insert_id(resource $conn_identifier = ?): string
```

Функция**cubrid\_insert\_id()** повертає ідентифікатор, згенерований для стовпця AUTO\_INCREMENT, що оновлюється попереднім запитом INSERT. Вона повертає 0, якщо попередній запит не генерує нові рядки або FALSE у разі виникнення помилки.

> **Зауваження** :
> 
> CUBRID підтримує AUTO\_INCREMENT для більш ніж одного стовпця у таблиці. У більшості випадків у таблиці буде один стовпець AUTO\_INCREMENT. Якщо є кілька стовпців AUTO\_INCREMENT, цю функцію не слід використовувати, навіть якщо вона поверне значення.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання, отриманий раніше під час виклику [cubrid\_connect()](function.cubrid-connect.md)

### Значення, що повертаються

Рядок, що представляє ідентифікатор, згенерований для стовпця AUTO\_INCREMENT попереднім запитом у разі успішного виконання.

0 якщо попередній запит не згенерував нові рядки.

\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.4.0 | Значення, що повертається у вигляді масиву замінено на рядок; Видалено перший параметр class\_name. |

### Приклади

**Пример #1 Пример использования**cubrid\_insert\_id()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

@cubrid_execute($conn, "DROP TABLE cubrid_test");
cubrid_execute($conn, "CREATE TABLE cubrid_test (d int AUTO_INCREMENT(1, 2), t varchar)");

for ($i = 0; $i < 10; $i++) {
    cubrid_execute($conn, "INSERT INTO cubrid_test(t) VALUES('cubrid_test')");
}

$id = cubrid_insert_id();
var_dump($id);

cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

```
string(2) "19"
```
