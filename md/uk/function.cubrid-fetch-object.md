---
navigation:
  - function.cubrid-fetch-lengths.md: « cubrid\_fetch\_lengths
  - function.cubrid-fetch-row.md: cubrid\_fetch\_row »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubrid\_fetch\_object
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_fetch\_object

(PECL CUBRID >= 8.3.0)

cubrid\_fetch\_object — Витягти наступний рядок як об'єкт

### Опис

```methodsynopsis
cubrid_fetch_object(    resource $result,    string $class_name = ?,    array $params = ?,    int $type = ?): object
```

Функція повертає об'єкт із властивостями, імена яких дорівнюють іменам стовпців результуючого набору, а значення відповідно значенням.

### Список параметрів

`result`

`Result` отриманий з [cubrid\_execute()](function.cubrid-execute.md)

`class_name`

Назва класу, який буде використаний для створення об'єкта. Якщо не задано, то буде використано [stdClass](class.stdclass.md) (stdClass - базовий, порожній клас PHP, який використовується при перетворенні інших типів в об'єкти).

`params`

Необов'язковий масив параметрів передачі в конструктор `class_name`

`type`

Може містити лише CUBRID\_LOB. Використовується під час роботи з об'єктами типу LOB.

### Значення, що повертаються

Об'єкт у разі успішного виконання.

\*\*`false`\*\*якщо рядків більше немає; \*\*`null`\*\*коли процес завершується з помилкою.

### Приклади

**Приклад #1 Приклад використання** cubrid\_fetch\_object()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$res = cubrid_execute($conn, "SELECT * FROM code");

var_dump(cubrid_fetch_object($res));

// В случае работы с LOB используйте cubrid_fetch_object($res, CUBRID_LOB)

class demodb_code {
    public $s_name = null;
    public $f_name = null;

    public function toString() {
        var_dump($this);
    }
}

var_dump(cubrid_fetch_object($res, "demodb_code"));

// В случае работы с LOB используйте cubrid_fetch_object($res, "demodb_code", CUBRID_LOB)

class demodb_code_construct extends demodb_code {
    public function __construct($s, $f) {
        $this->s_name = $s;
        $this->f_name = $f;
    }
}

var_dump(cubrid_fetch_object($res, 'demodb_code_construct', array('s_name', 'f_name')));

// В случае работы с LOB используйте cubrid_fetch_object($res, 'demodb_code_construct', array('s_name', 'f_name'), CUBRID_LOB)


var_dump(cubrid_fetch_object($res));

cubrid_close_request($res);
cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

```
object(stdClass)#1 (2) {
  ["s_name"]=>
  string(1) "X"
  ["f_name"]=>
  string(5) "Mixed"
}
object(demodb_code)#1 (2) {
  ["s_name"]=>
  string(1) "W"
  ["f_name"]=>
  string(5) "Woman"
}
object(demodb_code_construct)#1 (2) {
  ["s_name"]=>
  string(6) "s_name"
  ["f_name"]=>
  string(6) "f_name"
}
object(stdClass)#1 (2) {
  ["s_name"]=>
  string(1) "B"
  ["f_name"]=>
  string(6) "Bronze"
}
```

### Дивіться також

-   [cubrid\_execute()](function.cubrid-execute.md) \- Виконує підготовлений SQL-оператор
-   [cubrid\_fetch()](function.cubrid-fetch.md) \- Вибирає наступний рядок із набору результатів
-   [cubrid\_fetch\_array()](function.cubrid-fetch-array.md) \- Вилучення рядка з результуючого набору у вигляді асоціативного масиву, індексованого масиву або обох відразу
-   [cubrid\_fetch\_assoc()](function.cubrid-fetch-assoc.md) \- Витягти рядок із результуючого набору у вигляді асоціативного масиву
-   [cubrid\_fetch\_row()](function.cubrid-fetch-row.md) \- Витягти рядок із результуючого набору у вигляді індексованого масиву
