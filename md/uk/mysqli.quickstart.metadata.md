- [«API підтримка транзакцій](mysqli.quickstart.transactions.md)
- [Встановлення та налаштування »](mysqli.setup.md)

- [PHP Manual](index.md)
- [Короткий посібник](mysqli.quickstart.md)
- Метадані

## Метадані

Результуючий набір MySQL містить метадані. Ці дані описують
стовпці результуючої таблиці. Усі відомості, які передає MySQL,
доступні через `mysqli` інтерфейс. Модуль не змінює отримані дані,
або ці зміни незначні. Відмінності між версіями MySQL також
можна не брати до уваги.

Метадані доступні через інтерфейс
[mysqli_result](class.mysqli-result.md).

**Приклад #1 Доступ до метаданих результуючої таблиці**

` <?php$mysqli = new mysqli("example.com", "user", "password", "database");if ($mysqli->connect_errno) {    echo "Не удалося підключитися до| mysqli->connect_errno . ") " . $mysqli->connect_error;}$res = $mysqli->query("SELECT 1 AS _one, 'Hello' AS _two FROM DUAL");var_dump($res->fetch_fields());?> `

Результат виконання цього прикладу:

array(2) {
[0]=>
object(stdClass)#3 (13) {
["name"]=>
string(4) "_one"
["orgname"]=>
string(0) ""
["table"]=>
string(0) ""
["orgtable"]=>
string(0) ""
["def"]=>
string(0) ""
["db"]=>
string(0) ""
["catalog"]=>
string(3) "def"
["max_length"]=>
int(1)
["length"]=>
int(1)
["charsetnr"]=>
int(63)
["flags"]=>
int(32897)
["type"]=>
int(8)
["decimals"]=>
int(0)
}
[1]=>
object(stdClass)#4 (13) {
["name"]=>
string(4) "_two"
["orgname"]=>
string(0) ""
["table"]=>
string(0) ""
["orgtable"]=>
string(0) ""
["def"]=>
string(0) ""
["db"]=>
string(0) ""
["catalog"]=>
string(3) "def"
["max_length"]=>
int(5)
["length"]=>
int(5)
["charsetnr"]=>
int(8)
["flags"]=>
int(1)
["type"]=>
int(253)
["decimals"]=>
int(31)
}
}

*Підготовки запитів*

Метадані результуючих наборів, отриманих у результаті виконання
підготовлених запитів можна отримати аналогічним чином. Підходящий
дескриптор [mysqli_result](class.mysqli-result.md) можна отримати
функцією
[mysqli_stmt::result_metadata()](mysqli-stmt.result-metadata.md).

**Приклад #2 Метадані підготовлених запитів**

` <?phpmysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);$mysqli = new mysqli("example.com", "user", "password", "database");$stmt = $mysql 'Hello' AS _two FROM DUAL");$stmt->execute();$result = $stmt->result_metadata();var_dump($result->fetch_fields()); `

*Дивіться також*

- [mysqli::query()](mysqli.query.md)
- [mysqli_result::fetch_fields()](mysqli-result.fetch-fields.md)
