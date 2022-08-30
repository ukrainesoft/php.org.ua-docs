Встановлює внутрішній покажчик результату на передане усунення поля

-   [« mysqlfieldname](function.mysql-field-name.html)
    
-   [mysqlfieldtable »](function.mysql-field-table.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Встановлює внутрішній покажчик результату на передане усунення поля
    

# mysqlfieldseek

(PHP 4, PHP 5)

mysqlfieldseek - Встановлює внутрішній покажчик результату на передане зміщення поля

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDOMySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqlifieldseek()](mysqli-result.field-seek.html)
-   [PDOStatement::fetch()](pdostatement.fetch.html) з використанням параметрів `cursor_orientation` і `offset`

### Опис

```methodsynopsis
mysql_field_seek(resource $result, int $field_offset): bool
```

Переміщує покажчик до поля із зазначеним усуненням. Якщо наступний виклик функції [mysqlfetchfield()](function.mysql-fetch-field.html) не містить зміщення, то буде повернено зміщення, що міститься в **mysqlfieldseek()**

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.html). Цей результат можна отримати за допомогою функції [mysqlquery()](function.mysql-query.html)

`field_offset`

Числове усунення поля . `field_offset` починається з `0`. Якщо `field_offset` не існує, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [mysqlfetchfield()](function.mysql-fetch-field.html) - Повертає інформацію про колонку з результату запиту як об'єкта