Повертає наступне поле результуючого набору

-   [« mysqliresult::fetchfielddirect](mysqli-result.fetch-field-direct.html)
    
-   [mysqliresult::fetchfields »](mysqli-result.fetch-fields.html)
    
-   [PHP Manual](index.md)
    
-   [mysqliresult](class.mysqli-result.html)
    
-   Повертає наступне поле результуючого набору
    

# mysqliresult::fetchfield

# mysqlifetchfield

(PHP 5, PHP 7, PHP 8)

mysqliresult::fetchfield - mysqlifetchfield — Повертає наступне поле результуючого набору

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

Тільки для процедурного стилю: об'єкт [mysqliresult](class.mysqli-result.html), отриманий за допомогою [mysqliquery()](mysqli.query.md) [mysqlistoreresult()](mysqli.store-result.html) [mysqliuseresult()](mysqli.use-result.html) або [mysqlistmtgetresult()](mysqli-stmt.get-result.html)

### Значення, що повертаються

Повертає об'єкт, що містить визначення поля або \*\*`false`\*\*якщо стовпці в результуючій таблиці закінчилися.

**Властивості об'єкту**

| Свойство | Описание |
| --- | --- |
| name | Ім'я стовпця |
| orgname | Вихідне ім'я стовпця, якщо він має псевдонім |
| table | Ім'я таблиці, якій належить стовпець (якщо не обчислено) |
| orgtable | Початкове ім'я таблиці, якщо є псевдонім |
| def | Зарезервовано для стандартного значення, на даний момент завжди "" |
| дб | Ім'я бази даних |
| catalog | Ім'я каталогу завжди "def" |
| maxlength | Максимальна ширина поля результуючого набору. |
| length | Ширина поля, як вона задана щодо таблиці. |
| charsetnr | Кількість наборів символів для поля. |
| flags | Ціла кількість, що представляє бітові прапори для поля. |
| type | Тип даних поля |
| decimals | Число знаків після коми (для цілих полів) |

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

$query = "SELECT Name, SurfaceArea from Country ORDER BY Code LIMIT 5";

if ($result = $mysqli->query($query)) {

    /* Получим информацию обо всех столбцах */
    while ($finfo = $result->fetch_field()) {

        printf("Имя:         %s\n", $finfo->name);
        printf("Таблица:     %s\n", $finfo->table);
        printf("Макс. длина: %d\n", $finfo->max_length);
        printf("Флаги:       %d\n", $finfo->flags);
        printf("Тип:         %d\n\n", $finfo->type);
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

$query = "SELECT Name, SurfaceArea from Country ORDER BY Code LIMIT 5";

if ($result = mysqli_query($link, $query)) {

    /* Получим информацию обо всех столбцах */
    while ($finfo = mysqli_fetch_field($result)) {

        printf("Имя:         %s\n", $finfo->name);
        printf("Таблица:     %s\n", $finfo->table);
        printf("Макс. длина: %d\n", $finfo->max_length);
        printf("Флаги:       %d\n", $finfo->flags);
        printf("Тип:         %d\n\n", $finfo->type);    }
    mysqli_free_result($result);
}

/* закрываем подключение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

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

-   [mysqlinumfields()](mysqli-result.field-count.html) - Отримує кількість полів у наборі результатів
-   [mysqlifetchfielddirect()](mysqli-result.fetch-field-direct.html) - Отримання метаданих конкретного поля
-   [mysqlifetchfields()](mysqli-result.fetch-fields.html) - Повертає масив об'єктів, що становлять поля результуючого набору
-   [mysqlifieldseek()](mysqli-result.field-seek.html) - встановити покажчик поля на певне зміщення