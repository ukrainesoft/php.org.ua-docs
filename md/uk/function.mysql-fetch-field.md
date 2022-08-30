Повертає інформацію про колонку з результату запиту як об'єкта

-   [« mysqlfetchassoc](function.mysql-fetch-assoc.html)
    
-   [mysqlfetchlengths »](function.mysql-fetch-lengths.html)
    
-   [PHP Manual](index.md)
    
-   [MySQL](ref.mysql.md)
    
-   Повертає інформацію про колонку з результату запиту як об'єкта
    

# mysqlfetchfield

(PHP 4, PHP 5)

mysqlfetchfield — Повертає інформацію про колонку з результату запиту як об'єкт

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqlifetchfield()](mysqli-result.fetch-field.html)
-   [PDOStatement::getColumnMeta()](pdostatement.getcolumnmeta.md)

### Опис

```methodsynopsis
mysql_fetch_field(resource $result, int $field_offset = 0): object
```

Повертає об'єкт, що містить інформацію про колонку. Цю функцію можна використовувати для отримання інформації про поля у надісланому результаті запиту.

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysqlquery()](function.mysql-query.html)

`field_offset`

Числове усунення поля. Якщо усунення не вказано, функція повертає інформацію про першу колонку, яка ще не була оброблена цією функцією. Нумерація `field_offset` починається з `0`

### Значення, що повертаються

Повертає об'єкт, що містить інформацію про колонку. Об'єкт містить такі властивості:

-   name - назва колонки
-   table - назва таблиці, якій належить колонка, або псевдонім таблиці, якщо він був визначений
-   maxlength - максимальна довжина колонки
-   notnull - 1, якщо колонка не може бути **`null`**
-   primarykey - 1, якщо колонка є первинним індексом
-   uniquekey - 1, якщо колонка є унікальним індексом
-   multiplekey - 1, якщо колонка є унікальним індексом
-   numeric - 1, якщо колонка чисельна
-   blob - 1, якщо колонка є BLOB
-   type - тип колонки
-   unsigned - 1, якщо стовпчик не містить знака (unsigned)
-   zerofill - 1, якщо колонка заповнюється нулями (zero-filled)

### Приклади

**Приклад #1 Приклад використання **mysqlfetchfield()****

```php
<?php
$conn = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$conn) {
    die('Ошибка при соединении: ' . mysql_error());
}
mysql_select_db('database');
$result = mysql_query('select * from table');
if (!$result) {
    die('Ошибка в запросе: ' . mysql_error());
}
/* получаем данные о колонке */
$i = 0;
while ($i < mysql_num_fields($result)) {
    echo "Информация о колонке $i:<br />\n";
    $meta = mysql_fetch_field($result, $i);
    if (!$meta) {
        echo "Информация недоступна<br />\n";
    }
    echo "<pre>
blob:         $meta->blob
max_length:   $meta->max_length
multiple_key: $meta->multiple_key
name:         $meta->name
not_null:     $meta->not_null
numeric:      $meta->numeric
primary_key:  $meta->primary_key
table:        $meta->table
type:         $meta->type
unique_key:   $meta->unique_key
unsigned:     $meta->unsigned
zerofill:     $meta->zerofill
</pre>";
    $i++;
}
mysql_free_result($result);
?>
```

### Примітки

> **Зауваження**: Імена полів, що повертаються цією функцією *залежними від регістру*

> **Зауваження**
> 
> Якщо поля або таблиці мають додаткові імена у запиті SQL, буде повернено ці додаткові імена. Вихідне ім'я може бути отримано, наприклад, за допомогою [mysqliresult::fetchfield()](mysqli-result.fetch-field.html)

### Дивіться також

-   [mysqlfieldseek()](function.mysql-field-seek.html) - Встановлює внутрішній покажчик результату на передане усунення поля