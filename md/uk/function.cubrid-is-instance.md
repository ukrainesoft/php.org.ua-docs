---
navigation:
  - function.cubrid-insert-id.md: « cubrid\_insert\_id
  - function.cubrid-lob-close.md: cubrid\_lob\_close »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_is\_instance
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_is\_instance

(PECL CUBRID >= 8.3.0)

cubrid\_is\_instance — Перевіряє, чи існує екземпляр, на який вказує OID

### Опис

```methodsynopsis
cubrid_is_instance(resource $conn_identifier, string $oid): int
```

Функция**cubrid\_is\_instance()** використовується, щоб перевірити, чи існує екземпляр, на який вказує даний `oid`, чи ні.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`oid`

OID екземпляра, існування якого потрібно перевірити.

### Значення, що повертаються

1, якщо такий екземпляр існує;

0, якщо такого екземпляра немає;

\-1 у разі виникнення помилки.

### Приклади

**Пример #1 Пример использования**cubrid\_is\_instance()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

$sql = <<<EOD
SELECT host_year, medal, game_date
FROM game
WHERE athlete_code IN
    (SELECT code FROM athlete WHERE name='Thorpe Ian');
EOD;

$req = cubrid_execute($conn, $sql, CUBRID_INCLUDE_OID);
$oid = cubrid_current_oid($req);

$res = cubrid_is_instance ($conn, $oid);
if ($res == 1) {
    echo "Экземпляр, на который указывает $oid, существует.\n";
} else if ($res == 0){
    echo "Экземпляр, на который указывает $oid, не существует.\n";
} else {
    echo "Ошибка\n";
}

cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

```
Экземпляр, на который указывает @0|0|0, не существует.
```

### Дивіться також

-   [cubrid\_drop()](function.cubrid-drop.md) \- Видалення екземпляра за OID
-   [cubrid\_get\_class\_name()](function.cubrid-get-class-name.md) \- Отримує ім'я класу за допомогою OID
