Повертає останню помилку

-   [« ocidefineбname](function.oci-define-by-name.html)
    
-   [ociexecute »](function.oci-execute.html)
    
-   [PHP Manual](index.md)
    
-   [OCI8 Функции](ref.oci8.md)
    
-   Повертає останню помилку
    

# ocierror

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocierror — Повертає останню помилку

### Опис

```methodsynopsis
oci_error(?resource $connection_or_statement = null): array|false
```

Повертає останню знайдену помилку.

Функція повинна викликатися відразу після появи помилки. Помилки очищаються під час правильного запиту.

### Список параметрів

`connection_or_statement`

Для більшості помилок параметром `connection_or_statement` є відповідний ідентифікатор з'єднання або виразу. Для помилок під час виконання функцій [ociconnect()](function.oci-connect.html) [ocinewconnect()](function.oci-new-connect.html) або [ocipconnect()](function.oci-pconnect.html) слід передавати **`null`**

### Значення, що повертаються

Якщо помилок не знайдено, то **ocierror()** повертає **`false`**. В іншому випадку, **ocierror()** повертає інформацію про помилку як асоціативного масиву.

**Опис масиву виводу **ocierror()****

| Ключ Масива | Тип    | Описание                                                         |
|-------------|--------|------------------------------------------------------------------|
| `code`      | int    | Номер помилки Oracle.                                            |
| `message`   | string | Текст помилки Oracle.                                            |
| `offset`    | int    | Позиція помилки у запиті SQL. Якщо немає запиту, то дорівнює `0` |
| `sqltext`   | string | Текст запиту SQL. Якщо немає запиту, рядок порожній.             |

### список змін

| Версия                 | Описание                                                |
|------------------------|---------------------------------------------------------|
| 8.0.0, PECL OCI8 3.0.0 | `connection_or_statement` тепер допускає значення null. |

### Приклади

**Приклад #1 Виведення повідомлення про помилку Oracle після помилки з'єднання**

```php
<?php
$conn = oci_connect("hr", "welcome", "localhost/XE");
if (!$conn) {
    $e = oci_error();   // Для обработки ошибок oci_connect
    trigger_error(htmlentities($e['message']), E_USER_ERROR);
}
?>
```

**Приклад #2 Виведення повідомлення про помилку Oracle після помилки аналізу**

```php
<?php
$stid = oci_parse($conn, "select ' from dual");  // пропущенные кавычки
if (!$stid) {
    $e = oci_error($conn);  // Для обработки ошибок oci_parse
    trigger_error(htmlentities($e['message']), E_USER_ERROR);
}
?>
```

**Приклад #3 Виведення повідомлення про помилку Oracle, помилкового запиту та позиції помилки запуску запиту**

```php
<?php
$stid = oci_parse($conn, "select does_not_exist from dual");
$r = oci_execute($stid);
if (!$r) {
    $e = oci_error($stid);  // Для обработки ошибок oci_execute
    print htmlentities($e['message']);
    print "\n<pre>\n";
    print htmlentities($e['sqltext']);
    printf("\n%".($e['offset']+1)."s", "^");
    print  "\n</pre>\n";
}
?>
```