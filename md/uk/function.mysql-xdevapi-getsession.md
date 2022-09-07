---
navigation:
  - function.mysql-xdevapi-expression.md: « expression
  - class.mysql-xdevapi-baseresult.md: mysqlxdevapiBaseResult »
  - index.md: PHP Manual
  - ref.mysql-xdevapi.md: Функції Mysqlxdevapi
title: getSession
---
# getSession

(No version information available, might only be in Git)

getSession — Підключається до сервера MySQL

### Опис

```methodsynopsis
mysql_xdevapi\getSession(string $uri): mysql_xdevapi\Session
```

Підключається до MySQL.

### Список параметрів

`uri`

URI до сервера MySQL, як `mysqlx://user:password@host`

Формат URI:

`scheme://[user[:[password]]@]target[:port][?attribute1=value1&attribute2=value2...`

-   `scheme`: обов'язковий протокол з'єднання
    
    У mysqlxdevapi це завжди 'mysqlx' (для X Protocol)
    
-   `user`: необов'язковий, обліковий запис користувача MySQL для автентифікації
    
-   `password`: необов'язковий пароль користувача MySQL для аутентифікації
    
-   `target`: обов'язковий екземпляр сервера, до якого відноситься з'єднання:
    
    TCP-з'єднання (ім'я хоста, адреса IPv4 або IPv6)
    
    Шлях до сокету Unix (локальний шлях до файлу)
    
    Іменований канал Windows (локальний шлях до файлу)
    
-   `port`: необов'язковий, мережевий порт MySQL сервера.
    
    за замовчуванням порт для X Protocol дорівнює 33060
    
-   `?attribute=value`: цей елемент є необов'язковим та визначає словник даних, який містить різні параметри, у тому числі:
    
    -   Атрибут `auth` (механізм аутентифікації), оскільки він відноситься до зашифрованих з'єднань. Для отримання додаткової інформації дивіться [» Параметри команди для зашифрованих з'єднань](https://dev.mysql.com/doc/refman/8.0/en/encrypted-connection-options.md). Підтримуються такі значення: `plain` `mysql41` `external`, і `sha256_mem`
        
    -   Атрибут `connect-timeout` впливає з'єднання, а чи не на наступні операції. Він встановлюється для кожного з'єднання на одному або кількох хостах.
        
        Введіть позитивне ціле число, щоб визначити час очікування з'єднання в секундах, або введіть 0 (нуль), щоб вимкнути час очікування (нескінченно). Не визначаючи час очікування на підключення, ви використовуєте значення за замовчуванням 10.
        
        Пов'язані, змінні середовища MYSQLXCONNECTIONTIMEOUT (час очікування в секундах) та MYSQLXTESTCONNECTIONTIMEOUT (використовуються під час виконання тестів) можуть бути встановлені та використані замість connect-timeout з'єднання в URI. Параметр URI підключення до connect-timeout має пріоритет над змінними середовищами.
        
    -   Необов'язковий атрибут `compression` приймає такі значення: `preferred` (клієнт домовляється з сервером, щоб знайти підтримуваний алгоритм; з'єднання не стисло, якщо взаємно підтримуваний алгоритм не знайдено), `required` (як "preferred", але з'єднання розривається, якщо взаємно підтримуваний алгоритм не знайдено), або `disabled` (з'єднання не стисло). За замовчуванням використовується `preferred`
        
        Опцію було додано у версії 8.0.20.
        
    -   Необов'язковий атрибут `compression-algorithms` визначає бажані алгоритми стиснення (та їх кращий порядок використання): `zstd_stream`(псевдонім: zstd), `lz4_message` (псевдонім: lz4) або `deflate_stream` (псевдоніми: deflate чи zlib). За замовчуванням використовується порядок (залежно від доступності системи): lz4message, zstdstream, потім deflatestream. Наприклад, під час передачі compression-algorithms=lz4, zstdstream використовується lz4, якщо він доступний, інакше використовується zstdstream. Якщо обидва недоступні, поведінка залежить від значення стиснення, наприклад, якщо compression=required, збій з помилкою.
        
        Опцію було додано у версії 8.0.22.
        

**Приклад #1 Приклади URI**

```php
mysqlx://foobar
mysqlx://root@localhost?socket=%2Ftmp%2Fmysqld.sock%2F
mysqlx://foo:bar@localhost:33060
mysqlx://foo:bar@localhost:33160?ssl-mode=disabled
mysqlx://foo:bar@localhost:33260?ssl-mode=required
mysqlx://foo:bar@localhost:33360?ssl-mode=required&auth=mysql41
mysqlx://foo:bar@(/path/to/socket)
mysqlx://foo:bar@(/path/to/socket)?auth=sha256_mem
mysqlx://foo:bar@[localhost:33060, 127.0.0.1:33061]
mysqlx://foobar?ssl-ca=(/path/to/ca.pem)&ssl-crl=(/path/to/crl.pem)
mysqlx://foo:bar@[localhost:33060, 127.0.0.1:33061]?ssl-mode=disabled
mysqlx://foo:bar@localhost:33160/?connect-timeout=0
mysqlx://foo:bar@localhost:33160/?connect-timeout=10&compression=required
mysqlx://foo:bar@localhost:33160/?connect-timeout=10&compression=required&compression-algorithms=[lz4,zstd_stream]
```

Для отримання додаткової інформації дивіться MySQL Shell [» Подключение с использованием строки URI](https://dev.mysql.com/doc/refman/8.0/en/mysql-shell-connection-using-uri.md)

### Значення, що повертаються

Об'єкт **Session**

### Помилки

Помилка з'єднання викликає [Exception](class.exception.md)

### Приклади

**Приклад #2 Приклад використання **mysqlxdevapigetSession()****

```php
<?php
try {
    $session = mysql_xdevapi\getSession("mysqlx://user:password@host");
} catch(Exception $e) {
    die("Не удалось установить соединение: " . $e->getMessage());
}

$schemas = $session->getSchemas();
print_r($schemas);

$mysql_version = $session->getServerVersion();
print_r($mysql_version);

var_dump($collection->find("name = 'Alfred'")->execute()->fetchOne());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => mysql_xdevapi\Schema Object
        (
            [name] => helloworld
        )
    [1] => mysql_xdevapi\Schema Object
        (
            [name] => information_schema
        )
    [2] => mysql_xdevapi\Schema Object
        (
            [name] => mysql
        )
    [3] => mysql_xdevapi\Schema Object
        (
            [name] => performance_schema
        )
    [4] => mysql_xdevapi\Schema Object
        (
            [name] => sys
        )
)

80012

array(4) {
  ["_id"]=>
  string(28) "00005ad66abf0001000400000003"
  ["age"]=>
  int(42)
  ["job"]=>
  string(7) "Butler"
  ["name"]=>
  string(4) "Alfred"
}
```
