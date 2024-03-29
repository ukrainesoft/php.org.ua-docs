---
navigation:
  - function.cubrid-column-types.md: « cubrid\_column\_types
  - function.cubrid-connect-with-url.md: cubrid\_connect\_with\_url »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_commit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_commit

(PECL CUBRID >= 8.3.0)

cubrid\_commit — Підтвердження транзакції

### Опис

```methodsynopsis
cubrid_commit(resource $conn_identifier): bool
```

Функция**cubrid\_commit()** використовується для підтвердження змін, здійснених у транзакції у з'єднанні `conn_identifier`, після виклику функції **cubrid\_commit()**, з'єднання з сервером буде закрито, але обробник з'єднання все ще буде коректним.

У CUBRID PHP режим авто-комміту для транзакцій за замовчуванням вимкнено. Ви можете дозволити або заборонити його за допомогою функції [cubrid\_set\_autocommit()](function.cubrid-set-autocommit.md). Дізнатися поточний статус можна функцією [cubrid\_get\_autocommit()](function.cubrid-get-autocommit.md). Перед тим, як розпочати транзакцію, переконайтеся, що авто-коміт заборонено.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_commit()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

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
cubrid_set_autocommit($conn,false);
if (!cubrid_execute($conn, $sql)) {
    printf("Error facility: %d\nError code: %d\nError msg: %s\n", cubrid_error_code_facility(), cubrid_error_code(), cubrid_error_msg());

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

-   [cubrid\_rollback()](function.cubrid-rollback.md) \- Відкат транзакції
-   [cubrid\_get\_autocommit()](function.cubrid-get-autocommit.md) \- Повертає налаштування авто-комміту для з'єднання
-   [cubrid\_set\_autocommit()](function.cubrid-set-autocommit.md) \- Встановлює режим авто-комміту для з'єднання
