---
navigation:
  - function.ldap-connect-wallet.md: « ldap\_connect\_wallet
  - function.ldap-control-paged-result-response.md: ldap\_control\_paged\_result\_response »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_connect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_connect

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_connect — Підключається до сервера LDAP

### Опис

```methodsynopsis
ldap_connect(?string $uri = null): LDAP\Connection|false
```

**Увага**

Починаючи з PHP 8.3.0 *наступна*сигнатура устарела:

```methodsynopsis
ldap_connect(?string $host = null, int $port = 389): LDAP\Connection|false
```

Створює об'єкт [LDAP\\Connection](class.ldap-connection.md) та перевіряє правдоподібність заданого у параметрі `uri`значения.

> **Зауваження**: Ця функція *не* відкриває з'єднання. Вона перевіряє, чи правдоподібні задані параметри і чи можна, вказавши їх, встановити з'єднання, коли воно необхідне.

### Список параметрів

`host`

Повний LDAP URI виду `ldap://hostname:port`или`ldaps://hostname:port`

Можна також вказати кілька LDAP-URI, розділених пробілом.

Обратите внимание, что`hostname:port` — це LDAP URI, що не підтримується, оскільки відсутня схема.

`uri`

Ім'я сервера для з'єднання.

`port`

Порт для підключення.

### Значення, що повертаються

Повертає екземпляр [LDAP\\Connection](class.ldap-connection.md), якщо LDAP URI є правдоподібним. Вона здійснює синтаксичний аналіз та перевірку переданих параметрів, але з'єднання з сервером не відбувається. Якщо перевірка синтаксису провалилася - повертається **`false`**Функция**ldap\_connect()** завжди повертатиме екземпляр [LDAP\\Connection](class.ldap-connection.md)оскільки вона фактично не з'єднується, а лише ініціалізує параметри з'єднання. Фактичне підключення відбувається за наступних викликів функцій ldap\_\*зазвичай при виклику функції [ldap\_bind()](function.ldap-bind.md)

Якщо жодних параметрів не буде визначено, тоді буде повернуто екземпляр відкритого з'єднання.[LDAP\\Connection](class.ldap-connection.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Тепер виклик функції **ldap\_connect()** з окремою вказівкою імені хоста `hostname` та порту `port`устарел. |
| 8.1.0 | Повертає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше повертався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад підключення до LDAP-сервера.**

```php
<?php

// LDAP переменные
$ldapuri = "ldap://ldap.example.com:389";  // ldap-uri

// Соединение с LDAP
$ldapconn = ldap_connect($ldapuri)
          or die("LDAP-URI некорректен");

?>
```

**Приклад #2 Приклад безпечного підключення до LDAP-сервера.**

```php
<?php

// Убедитесь, что ваш хост корректный и
// что вы выдали ему сертификат безопасности
$ldaphost = "ldaps://ldap.example.com/";

// Соединение с LDAP
$ldapconn = ldap_connect($ldaphost)
          or die("LDAP-URI некорректен");

?>
```

### Дивіться також

-   [ldap\_bind()](function.ldap-bind.md) \- Прив'язати до LDAP директорії
