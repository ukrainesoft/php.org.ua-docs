---
navigation:
  - mysqli-result.getiterator.html: '« mysqliresult::getIterator'
  - mysqli-result.num-rows.html: 'mysqliresult::$numrows »'
  - index.html: PHP Manual
  - class.mysqli-result.html: mysqliresult
title: 'mysqliresult::$lengths'
---
# mysqliresult::$lengths

# mysqlifetchlengths

(PHP 5, PHP 7, PHP 8)

mysqliresult::$lengths -- mysqlifetchlengths — Повертає довжини полів поточного рядка результуючого набору

### Опис

Об'єктно-орієнтований стиль

?array [$mysqliresult->lengths](mysqli-result.lengths.md)

Процедурний стиль

```methodsynopsis
mysqli_fetch_lengths(mysqli_result $result): array|false
```

**mysqlifetchlengths()** повертає масив, елементи якого являють собою довжини кожного поля поточного рядка результуючого набору.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqliresult](class.mysqli-result.html), отриманий за допомогою [mysqliquery()](mysqli.query.html) [mysqlistoreresult()](mysqli.store-result.html) [mysqliuseresult()](mysqli.use-result.html) або [mysqlistmtgetresult()](mysqli-stmt.get-result.md)

### Значення, що повертаються

Масив цілих чисел, що становлять розміри значень стовпців (за винятком будь-яких завершальних нуль-символів) . **`false`** у разі виникнення помилки.

**mysqlifetchlengths()** відноситься лише до поточного рядка. Функція поверне **`false`**, якщо буде викликано до виклику mysqlifetchrow/array/object або якщо в результуючому наборі немає рядків.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* проверка подключения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

$query = "SELECT * from Country ORDER BY Code LIMIT 1";

if ($result = $mysqli->query($query)) {

    $row = $result->fetch_row();

    /* выведем длины полей */
    foreach ($result->lengths as $i => $val) {
        printf("Поле %2d имеет длину %2d\n", $i+1, $val);
    }
    $result->close();
}

/* закрываем подключение */
$mysqli->close();
?>
```

**Приклад #2 Процедурний стиль**

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* проверка подключения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

$query = "SELECT * from Country ORDER BY Code LIMIT 1";

if ($result = mysqli_query($link, $query)) {

    $row = mysqli_fetch_row($result);

    /* выведем длины полей */
    foreach (mysqli_fetch_lengths($result) as $i => $val) {
        printf("Поле %2d имеет длину %2d\n", $i+1, $val);
    }
    mysqli_free_result($result);
}

/* закрываем подключение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Поле  1 имеет длину  3
Поле  2 имеет длину  5
Поле  3 имеет длину 13
Поле  4 имеет длину  9
Поле  5 имеет длину  6
Поле  6 имеет длину  1
Поле  7 имеет длину  6
Поле  8 имеет длину  4
Поле  9 имеет длину  6
Поле 10 имеет длину  6
Поле 11 имеет длину  5
Поле 12 имеет длину 44
Поле 13 имеет длину  7
Поле 14 имеет длину  3
Поле 15 имеет длину  2
```
