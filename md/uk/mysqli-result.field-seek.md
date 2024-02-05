---
navigation:
  - mysqli-result.field-count.md: '« mysqli\_result::$field\_count'
  - mysqli-result.free.md: 'mysqli\_result::free »'
  - index.md: PHP Manual
  - class.mysqli-result.md: mysqli\_result
title: 'mysqli\_result::field\_seek'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_result::field\_seek

# mysqli\_field\_seek

(PHP 5, PHP 7, PHP 8)

mysqli\_result::field\_seek -- mysqli\_field\_seek — Встановити вказівник поля на певне усунення

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_result::field_seek(int $index): bool
```

Процедурний стиль

```methodsynopsis
mysqli_field_seek(mysqli_result $result, int $index): bool
```

Встановлює вказівник поля на задане усунення. Наступний виклик [mysqli\_fetch\_field()](mysqli-result.fetch-field.md) дозволить отримати інформацію про стовпчик з позицією усунення.

> **Зауваження** :
> 
> Для пошуку з початку рядка необхідно встановити нульове значення усунення.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqli\_result](class.mysqli-result.md), який повернула функція [mysqli\_query()](mysqli.query.md) [mysqli\_store\_result()](mysqli.store-result.md) [mysqli\_use\_result()](mysqli.use-result.md) або [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.md)

`index`

Номер поля. Це значення має бути в наступному діапазоні: від до`число полів – 1`

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція тепер завжди повертає значення **`true`**. . Раніше вона повертала значення \*\*`false`\*\*в случае возникновения ошибки. |

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* Проверить соединение */
if (mysqli_connect_errno()) {
    printf("Ошибка соединения: %s\n", mysqli_connect_error());
    exit();
}

$query = "SELECT Name, SurfaceArea from Country ORDER BY Code LIMIT 5";

if ($result = $mysqli->query($query)) {

    /* Получить информацию о поле во втором столбце */
    $result->field_seek(1);
    $finfo = $result->fetch_field();

    printf("Имя:     %s\n", $finfo->name);
    printf("Таблица:    %s\n", $finfo->table);
    printf("Макс. длина: %d\n", $finfo->max_length);
    printf("Флаги:    %d\n", $finfo->flags);
    printf("Тип:     %d\n\n", $finfo->type);

    $result->close();
}

/* Закрыть соединение */
$mysqli->close();
?>
```

**Приклад #2 Процедурний стиль**

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* Проверить соединение */
if (mysqli_connect_errno()) {
    printf("Ошибка соединения: %s\n", mysqli_connect_error());
    exit();
}

$query = "SELECT Name, SurfaceArea from Country ORDER BY Code LIMIT 5";

if ($result = mysqli_query($link, $query)) {

    /* Получить информацию о поле во втором столбце */
    mysqli_field_seek($result, 1);
    $finfo = mysqli_fetch_field($result);

    printf("Имя:     %s\n", $finfo->name);
    printf("Таблица:    %s\n", $finfo->table);
    printf("Макс. длина: %d\n", $finfo->max_length);
    printf("Флаги:    %d\n", $finfo->flags);
    printf("Тип:     %d\n\n", $finfo->type);

    mysqli_free_result($result);
}

/* Закрыть соединение */
mysqli_close($link);
?>
```

Результат виконання наведених прикладів:

```
Имя:     SurfaceArea
Таблица:    Country
Макс. длина: 10
Флаги:    32769
Тип:     4
```

### Дивіться також

-   [mysqli\_fetch\_field()](mysqli-result.fetch-field.md) \- Повертає наступне поле результуючого набору
