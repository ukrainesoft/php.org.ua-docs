Отримує інформацію про властивості полів бази даних

-   [« dbasedeleterecord](function.dbase-delete-record.html)
    
-   [dbasegetrecordwithnames »](function.dbase-get-record-with-names.html)
    
-   [PHP Manual](index.html)
    
-   [dBase](ref.dbase.html)
    
-   Отримує інформацію про властивості полів бази даних
    

# dbasegetheaderinfo

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbasegetheaderinfo — Отримує інформацію про властивості полів бази даних

### Опис

```methodsynopsis
dbase_get_header_info(resource $database): array
```

Повертає інформацію про структуру полів (стовпців) даного ресурсу бази даних.

### Список параметрів

`database`

Ресурс бази даних, отриманий за допомогою [dbaseopen()](function.dbase-open.html) або [dbasecreate()](function.dbase-create.html)

### Значення, що повертаються

Індексований масив значень кожної колонки (поля). Індекс масиву починається з 0.

Кожен елемент масиву містить асоціативний масив інформації про стовпці БД наступного виду:

name

Найменування поля

type

Тип поля dBase в зручному для сприйняття вигляді (date, boolean, і т.д.) типи файлів, що підтримуються, перераховані в [вступної секції](intro.dbase.html)

length

Максимальна кількість байт даного поля, що зберігається (включаючи "precision" - прим. пров.)

precision

Кількість цифр після коми

format

Запропонований у [printf()](function.printf.html) формат специфікації для цього типу

offset

Байт усунення, що вказує розміщення поля від початку запису (рядки).

Якщо інформація в заголовку бази даних не може бути прочитана, повертає **`false`**

### список змін

| Версия | Описание |
| --- | --- |
| dbase 7.0.0 | Параметр `database` тепер має тип resource, а не int. |

### Приклади

**Приклад #1 Отримання властивостей полів файлу бази даних dBase**

```php
<?php
// Путь к файлу БД
$db_path = "/tmp/test.dbf";

// Открываем файл БД
$dbh = dbase_open($db_path, 0)
  or die("Ошибка! Не получается открыть файл '$db_path'.");

// Получаем информацию о столбцах
$column_info = dbase_get_header_info($dbh);

// Отображение информации
print_r($column_info);
?>
```