---
navigation:
  - function.mysql-client-encoding.md: « mysql\_client\_encoding
  - function.mysql-connect.md: mysql\_connect »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_close

(PHP 4, PHP 5)

mysql\_close — Закриває з'єднання з сервером MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_close()](mysqli.close.md)
-   PDO: Присвоїти значення\*\*`null`\*\*об'єкту PDO

### Опис

```methodsynopsis
mysql_close(resource $link_identifier = NULL): bool
```

**mysql\_close()** закриває непостійне з'єднання з базою даних MySQL, яке вказує переданий дескриптор. Якщо параметр `link_identifier` не вказано, закривається останнє відкрите (поточне) з'єднання.

Відкриті непостійні з'єднання MySQL та результуючі набори автоматично видаляються відразу після закінчення роботи PHP-скрипту. Отже, закривати з'єднання і очищати результуючі набори не обов'язково, але рекомендується, оскільки це відразу звільнить ресурси бази даних і пам'ять, що займається результатами вибірки, що може позитивно позначитися на продуктивності. Більше інформації можна отримати в розділі [Визволення ресурсів](language.types.resource.md#language.types.resource.self-destruct)

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо з'єднання не знайдено або не встановлено, то буде згенеровано помилку рівня **`E_WARNING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** mysql\_close()\*\*\*\*

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
echo 'Успешно соединились';
mysql_close($link);
?>
```

Результат виконання наведеного прикладу:

```
Успешно соединились
```

### Примітки

> **Зауваження** :
> 
> **mysql\_close()** не закриває постійні з'єднання, створені функцією [mysql\_pconnect()](function.mysql-pconnect.md)Для дополнительной информации смотрите руководство по[постійним з'єднанням](features.persistent-connections.md)

### Дивіться також

-   [mysql\_connect()](function.mysql-connect.md) \- Відкриває з'єднання із сервером MySQL
-   [mysql\_free\_result()](function.mysql-free-result.md) \- Звільняє пам'ять від результату запиту
