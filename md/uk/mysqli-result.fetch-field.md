---
navigation:
  - mysqli-result.fetch-field-direct.md: '« mysqli\_result::fetch\_field\_direct'
  - mysqli-result.fetch-fields.md: 'mysqli\_result::fetch\_fields »'
  - index.md: PHP Manual
  - class.mysqli-result.md: mysqli\_result
title: 'mysqli\_result::fetch\_field'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_result::fetch\_field

# mysqli\_fetch\_field

(PHP 5, PHP 7, PHP 8)

mysqli\_result::fetch\_field -- mysqli\_fetch\_field — Повертає наступне поле результуючого набору

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_result::fetch_field(): object|false
```

Процедурний стиль

```methodsynopsis
mysqli_fetch_field(mysqli_result $result): object|false
```

Повертає інформацію про один стовпчик результуючого набору у вигляді об'єкта. Щоб отримати визначення всіх стовпців, просто запустіть цю функцію багаторазово.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqli\_result](class.mysqli-result.md), який повернула функція [mysqli\_query()](mysqli.query.md) [mysqli\_store\_result()](mysqli.store-result.md) [mysqli\_use\_result()](mysqli.use-result.md) або [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.md)

### Значення, що повертаються

Повертає об'єкт, що містить визначення поля або \*\*`false`\*\*якщо стовпці в результуючій таблиці закінчилися.

**Властивості об'єкту**

| Свойство | Опис |
| --- | --- |
| name | Ім'я стовпця |
| orgname | Вихідне ім'я стовпця, якщо він має псевдонім |
| table | Ім'я таблиці, якій належить стовпець (якщо не обчислено) |
| orgtable | Початкове ім'я таблиці, якщо є псевдонім |
| def | Зарезервовано для стандартного значення, на даний момент завжди "" |
| db | Ім'я бази даних |
| catalog | Ім'я каталогу завжди "def" |
| max\_length | Максимальна ширина поля результуючого набору. |
| length | Ширина поля, як вона задана щодо таблиці. |
| charsetnr | Кількість наборів символів для поля. |
| flags | Ціла кількість, що представляє бітові прапори для поля. |
| type | Тип даних поля |
| decimals | Число знаків після коми (для цілих полів) |

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* проверка подключения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

$query = "SELECT Name, SurfaceArea from Country ORDER BY Code LIMIT 5";

if ($result = $mysqli->query($query)) {

    /* Получим информацию обо всех столбцах */
    while ($finfo = $result->fetch_field()) {

        printf("Имя:         %s\n", $finfo->name);
        printf("Таблица:     %s\n", $finfo->table);
        printf("Макс. длина: %d\n", $finfo->max_length);
        printf("Флаги:       %d\n", $finfo->flags);
        printf("Тип:         %d\n\n", $finfo->type);
    }
    $result->close();
}

/* закрываем подключение */
$mysqli->close();
?>
```

**Приклад #2 Процедурний стиль**

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* проверка подключения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

$query = "SELECT Name, SurfaceArea from Country ORDER BY Code LIMIT 5";

if ($result = mysqli_query($link, $query)) {

    /* Получим информацию обо всех столбцах */
    while ($finfo = mysqli_fetch_field($result)) {

        printf("Имя:         %s\n", $finfo->name);
        printf("Таблица:     %s\n", $finfo->table);
        printf("Макс. длина: %d\n", $finfo->max_length);
        printf("Флаги:       %d\n", $finfo->flags);
        printf("Тип:         %d\n\n", $finfo->type);    }
    mysqli_free_result($result);
}

/* закрываем подключение */
mysqli_close($link);
?>
```

Результат виконання наведених прикладів:

```
Имя:         Name
Таблица:     Country
Макс. длина: 11
Флаги:       1
Тип:         254

Имя:         SurfaceArea
Таблица:     Country
Макс. длина: 10
Флаги:       32769
Тип:         4
```

### Дивіться також

-   [mysqli\_num\_fields()](mysqli-result.field-count.md) \- Отримує кількість полів у наборі результатів
-   [mysqli\_fetch\_field\_direct()](mysqli-result.fetch-field-direct.md) \- Отримання метаданих конкретного поля
-   [mysqli\_fetch\_fields()](mysqli-result.fetch-fields.md) \- Повертає масив об'єктів, що становлять поля результуючого набору
-   [mysqli\_field\_seek()](mysqli-result.field-seek.md) \- встановити покажчик поля на певне зміщення
