Закриває з'єднання з сервером MySQL

-   [« mysql\_client\_encoding](function.mysql-client-encoding.html)
    
-   [mysql\_connect »](function.mysql-connect.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Закриває з'єднання з сервером MySQL
    

# mysqlclose

(PHP 4, PHP 5)

mysqlclose — Закриває з'єднання з сервером MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDO\_MySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqli\_close()](mysqli.close.html)
-   PDO: Присвоїти значення **`null`** об'єкту PDO

### Опис

```methodsynopsis
mysql_close(resource $link_identifier = NULL): bool
```

**mysqlclose()** закриває непостійне з'єднання з базою даних MySQL, яке вказує переданий дескриптор. Якщо параметр `link_identifier` не вказано, закривається останнє відкрите (поточне) з'єднання.

Відкриті непостійні з'єднання MySQL та результуючі набори автоматично видаляються відразу після закінчення роботи PHP-скрипту. Отже, закривати з'єднання і очищати результуючі набори не обов'язково, але рекомендується, оскільки це відразу звільнить ресурси бази даних і пам'ять, що займається результатами вибірки, що може позитивно позначитися на продуктивності. Більше інформації можна отримати в розділі [Освобождение ресурсов](language.types.resource.html#language.types.resource.self-destruct)

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо не вказано, використовується останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.html). Якщо з'єднання не знайдено або не встановлено, то буде згенеровано помилку рівня **`E_WARNING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqlclose()****

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
echo 'Успешно соединились';
mysql_close($link);
?>
```

Результат виконання цього прикладу:

```
Успешно соединились
```

### Примітки

> **Зауваження**
> 
> **mysqlclose()** не закриває постійні з'єднання, створені функцією [mysql\_pconnect()](function.mysql-pconnect.html). Для додаткової інформації дивіться посібник з [постоянным соединениям](features.persistent-connections.html)

### Дивіться також

-   [mysql\_connect()](function.mysql-connect.html) - Відкриває з'єднання із сервером MySQL
-   [mysql\_free\_result()](function.mysql-free-result.html) - Звільняє пам'ять від результату запиту