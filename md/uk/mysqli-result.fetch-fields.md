Повертає масив об'єктів, що становлять поля результуючого набору

-   [« mysqliresult::fetchfield](mysqli-result.fetch-field.html)
    
-   [mysqliresult::fetchobject »](mysqli-result.fetch-object.html)
    
-   [PHP Manual](index.md)
    
-   [mysqliresult](class.mysqli-result.html)
    
-   Повертає масив об'єктів, що становлять поля результуючого набору
    

# mysqliresult::fetchfields

# mysqlifetchfields

(PHP 5, PHP 7, PHP 8)

mysqliresult::fetchfields - mysqlifetchfields — Повертає масив об'єктів, що становлять поля результуючого набору

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_result::fetch_fields(): array
```

Процедурний стиль

```methodsynopsis
mysqli_fetch_fields(mysqli_result $result): array
```

Ця функція служить для тих же цілей, що й [mysqlifetchfield()](mysqli-result.fetch-field.html), З тією лише різницею, що повертає не один об'єкт для стовпця, а масив таких об'єктів.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqliresult](class.mysqli-result.html), отриманий за допомогою [mysqliquery()](mysqli.query.md) [mysqlistoreresult()](mysqli.store-result.html) [mysqliuseresult()](mysqli.use-result.html) або [mysqlistmtgetresult()](mysqli-stmt.get-result.html)

### Значення, що повертаються

Повертає масив об'єктів, що містять метадані полів.

**Властивості об'єкту**

| Свойство | Описание |
| --- | --- |
| name | Ім'я стовпця |
| orgname | Вихідне ім'я стовпця, якщо він має псевдонім |
| table | Ім'я таблиці, якій належить стовпець (якщо не обчислено) |
| orgtable | Початкове ім'я таблиці, якщо є псевдонім |
| maxlength | Максимальна ширина поля результуючого набору. |
| length | Довжина поля в байтах, як вона поставлена ​​при визначенні таблиці. Зверніть увагу, що дана величина (в байтах) може відрізнятися від величини символів, зазначеної у визначенні поля таблиці, так як в різних кодуваннях один символ може записуватися кількома байтами. Наприклад, набір символів utf8 має 3 байти на символ, таким чином поле VARCHAR(10) у кодуванні UTF-8 поверне довжину 30 байтів = 10 символів. 3 байти на символ, а кодування LATIN1 - довжину 10, оскільки у цьому кодуванні один символ займає один байт. |
| charsetnr | Числовий ідентифікатор кодування. |
| flags | Ціла кількість, що представляє бітові прапори для поля. |
| type | Тип даних поля |
| decimals | Число знаків після коми (для цілих полів) |

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$mysqli = new mysqli("127.0.0.1", "root", "foofoo", "sakila");

/* Проверяем соединение */
if ($mysqli->connect_errno) {
    printf("Connect failed: %s\n", $mysqli->connect_error);
    exit();
}

foreach (array('latin1', 'utf8') as $charset) {

    // Устанавливаем кодировку для демонстрации её влияния на некоторые
    $mysqli->set_charset($charset);

    $query = "SELECT actor_id, last_name from actor ORDER BY actor_id";

    echo "======================\n";
    echo "Character Set: $charset\n";
    echo "======================\n";

    if ($result = $mysqli->query($query)) {

        /* Читаем информацию по всем столбцам */
        $finfo = $result->fetch_fields();

        foreach ($finfo as $val) {
            printf("Name:      %s\n",   $val->name);
            printf("Table:     %s\n",   $val->table);
            printf("Max. Len:  %d\n",   $val->max_length);
            printf("Length:    %d\n",   $val->length);
            printf("charsetnr: %d\n",   $val->charsetnr);
            printf("Flags:     %d\n",   $val->flags);
            printf("Type:      %d\n\n", $val->type);
        }
        $result->free();
    }
}
$mysqli->close();
?>
```

**Приклад #2 Процедурний стиль**

```php
<?php
$link = mysqli_connect("127.0.0.1", "my_user", "my_password", "sakila");

/* Проверяем соединение */
if (mysqli_connect_errno()) {
    printf("Connect failed: %s\n", mysqli_connect_error());
    exit();
}

foreach (array('latin1', 'utf8') as $charset) {

    // Устанавливаем кодировку для демонстрации её влияния на некоторые
    mysqli_set_charset($link, $charset);

    $query = "SELECT actor_id, last_name from actor ORDER BY actor_id";

    echo "======================\n";
    echo "Character Set: $charset\n";
    echo "======================\n";

    if ($result = mysqli_query($link, $query)) {

        /* Читаем информацию по всем столбцам */
        $finfo = mysqli_fetch_fields($result);

        foreach ($finfo as $val) {
            printf("Name:      %s\n",   $val->name);
            printf("Table:     %s\n",   $val->table);
            printf("Max. Len:  %d\n",   $val->max_length);
            printf("Length:    %d\n",   $val->length);
            printf("charsetnr: %d\n",   $val->charsetnr);
            printf("Flags:     %d\n",   $val->flags);
            printf("Type:      %d\n\n", $val->type);
        }
        mysqli_free_result($result);
    }
}

mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
======================
Character Set: latin1
======================
Name:      actor_id
Table:     actor
Max. Len:  3
Length:    5
charsetnr: 63
Flags:     49699
Type:      2

Name:      last_name
Table:     actor
Max. Len:  12
Length:    45
charsetnr: 8
Flags:     20489
Type:      253

======================
Character Set: utf8
======================
Name:      actor_id
Table:     actor
Max. Len:  3
Length:    5
charsetnr: 63
Flags:     49699
Type:      2

Name:      last_name
Table:     actor
Max. Len:  12
Length:    135
charsetnr: 33
Flags:     20489
```

### Дивіться також

-   [mysqlinumfields()](mysqli-result.field-count.html) - Отримує кількість полів у наборі результатів
-   [mysqlifetchfielddirect()](mysqli-result.fetch-field-direct.html) - Отримання метаданих конкретного поля
-   [mysqlifetchfield()](mysqli-result.fetch-field.html) - Повертає наступне поле результуючого набору