Підключитись до сервера LDAP

-   [« ldap\_compare](function.ldap-compare.html)
    
-   [ldap\_control\_paged\_result\_response »](function.ldap-control-paged-result-response.html)
    
-   [PHP Manual](index.html)
    
-   [Функции LDAP](ref.ldap.html)
    
-   Підключитись до сервера LDAP
    

# ldapconnect

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapconnect — З'єднатися з сервером LDAP

### Опис

```methodsynopsis
ldap_connect(?string $uri = null): LDAP\Connection|false
```

**Увага**

*Наступний* синтаксис все ще підтримується для забезпечення зворотної сумісності (крім використання іменованих аргументів), але він оголошений застарілим і не повинен використовуватися!

```methodsynopsis
ldap_connect(?string $uri = null, int $port = 389): LDAP\Connection|false
```

Створює [LDAP\\Connection](class.ldap-connection.html) та перевіряє правдоподібність заданого `uri`

> **Зауваження**: Ця функція *НЕ* відкриває з'єднання. Вона перевіряє, чи правдоподібні задані параметри і чи можуть використовуватися для підключення, коли в ньому виникне потрібна.

### Список параметрів

`uri`

Повний LDAP URI виду `ldap://hostname:port` або `ldaps://hostname:port`

Також можна вказати кілька LDAP-URI, розділених пробілом.

Зверніть увагу, що `hostname:port` - це LDAP URI, що не підтримується, оскільки відсутня схема.

`uri`

Ім'я сервера для з'єднання.

`port`

Порт для підключення.

### Значення, що повертаються

Повертає екземпляр [LDAP\\Connection](class.ldap-connection.html)якщо LDAP URI правдоподібний. Вона здійснює синтаксичний аналіз та перевірку переданих параметрів, але з'єднання з сервером не відбувається. Якщо перевірка синтаксису провалилася – повертається **`false`**. . **ldapconnect()** завжди повертатиме екземпляр [LDAP\\Connection](class.ldap-connection.html)оскільки вона фактично не з'єднується, а лише ініціалізує параметри з'єднання. Фактичне підключення відбувається за наступних викликів ldap функцій, зазвичай під час виклику [ldap\_bind()](function.ldap-bind.html)

Якщо жодних параметрів не буде визначено, тоді буде повернено екземпляр [LDAP\\Connection](class.ldap-connection.html) відкритого з'єднання.

### список змін

| Версия | Описание |
| --- | --- |
|  | Повертає екземпляр [LDAP\\Connection](class.ldap-connection.html); раніше повертався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад підключення до LDAP-сервера.**

```php
<?php

// LDAP переменные
$ldapuri = "ldap://ldap.example.com:389";  // ldap-uri

// Соединение с LDAP
$ldapconn = ldap_connect($ldapuri)
          or die("LDAP-URI некорректен");

?>
```

**Приклад #2 Приклад безпечного підключення до LDAP-сервера.**

```php
<?php

// Убедитесь, что ваш хост корректный и
// что вы выдали ему сертификат безопасности
$ldaphost = "ldaps://ldap.example.com/";

// Соединение с LDAP
$ldapconn = ldap_connect($ldaphost)
          or die("LDAP-URI некорректен");

?>
```

### Дивіться також

-   [ldap\_bind()](function.ldap-bind.html) - Прив'язати до LDAP директорії