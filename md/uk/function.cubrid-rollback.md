---
navigation:
  - function.cubrid-put.md: « cubrid\_put
  - function.cubrid-schema.md: cubrid\_schema »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_rollback
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_rollback

(PECL CUBRID >= 8.3.0)

cubrid\_rollback - Відкат транзакції

### Опис

```methodsynopsis
cubrid_rollback(resource $conn_identifier): bool
```

Функция**cubrid\_rollback()** виконує відкат транзакції, яку вказує `conn_identifier`, яка в даний момент виконується.

З'єднання з сервером закривається після дзвінка **cubrid\_rollback()**. Однак дескриптор з'єднання все ще дійсний.

### Список параметрів

`conn_identifier`

Connection identifier.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_rollback()\*\*\*\*

```php
<?php
$conn = cubrid_connect("127.0.0.1", 33000, "demodb", "dba");
cubrid_set_autocommit($conn,false);

@cubrid_execute($conn, "DROP TABLE publishers");

$sql = <<<EOD
CREATE TABLE publishers(
pub_id CHAR(3),
pub_name VARCHAR(20),
city VARCHAR(15),
state CHAR(2),
country VARCHAR(15)
)
EOD;

if (!cubrid_execute($conn, $sql)) {
    printf("Ошибка объекта: %d\nКод ошибки: %d\nСообщение об ошибке: %s\n", cubrid_error_code_facility(), cubrid_error_code(), cubrid_error_msg());

    cubrid_disconnect($conn);
    exit;
}

$req = cubrid_prepare($conn, "INSERT INTO publishers VALUES(?, ?, ?, ?, ?)");

$id_list = array("P01", "P02", "P03", "P04");
$name_list = array("Abatis Publishers", "Core Dump Books", "Schadenfreude Press", "Tenterhooks Press");
$city_list = array("New York", "San Francisco", "Hamburg", "Berkeley");
$state_list = array("NY", "CA", NULL, "CA");
$country_list = array("USA", "USA", "Germany", "USA");

for ($i = 0, $size = count($id_list); $i < $size; $i++) {
    cubrid_bind($req, 1, $id_list[$i]);
    cubrid_bind($req, 2, $name_list[$i]);
    cubrid_bind($req, 3, $city_list[$i]);
    cubrid_bind($req, 4, $state_list[$i]);
    cubrid_bind($req, 5, $country_list[$i]);

    if (!($ret = cubrid_execute($req))) {
        break;
    }
}

if (!$ret) {
    cubrid_rollback($conn);
} else {
    cubrid_commit($conn);

    $req = cubrid_execute($conn, "SELECT * FROM publishers");
    while ($result = cubrid_fetch_assoc($req)) {
        printf("%-3s %-20s %-15s %-3s %-15s\n",
            $result["pub_id"], $result["pub_name"], $result["city"], $result["state"], $result["country"]);
    }
}

cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

```
P01 Abatis Publishers    New York        NY  USA
P02 Core Dump Books      San Francisco   CA  USA
P03 Schadenfreude Press  Hamburg             Germany
P04 Tenterhooks Press    Berkeley        CA  USA
```

### Дивіться також

-   [cubrid\_commit()](function.cubrid-commit.md) \- підтвердження транзакції
-   [cubrid\_disconnect()](function.cubrid-disconnect.md) \- Закриває з'єднання з базою даних
