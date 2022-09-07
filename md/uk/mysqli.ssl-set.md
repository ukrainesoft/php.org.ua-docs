---
navigation:
  - mysqli.sqlstate.md: '« mysqli::$sqlstate'
  - mysqli.stat.md: 'mysqli::stat »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::sslset'
---
# mysqli::sslset

# mysqlisslset

(PHP 5, PHP 7, PHP 8)

mysqli::sslset - mysqlisslset — Використовується для встановлення безпечних з'єднань за допомогою SSL

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::ssl_set(    ?string $key,    ?string $certificate,    ?string $ca_certificate,    ?string $ca_path,    ?string $cipher_algos): bool
```

Процедурний стиль

```methodsynopsis
mysqli_ssl_set(    mysqli $mysql,    ?string $key,    ?string $certificate,    ?string $ca_certificate,    ?string $ca_path,    ?string $cipher_algos): bool
```

Використовується для встановлення безпечних з'єднань за допомогою SSL. Функцію необхідно викликати до дзвінка [mysqlirealconnect()](mysqli.real-connect.md). Для роботи функції потрібно включити підтримку OpenSSL, інакше функція робити нічого не буде.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.md) або [mysqliinit()](mysqli.init.md)

`key`

Шлях та ім'я ключового файлу.

`certificate`

Шлях та ім'я файлу сертифіката.

`ca_certificate`

Шлях та ім'я файлу з дозволами сертифіката.

`ca_path`

Шлях до директорії, де зберігаються довірені CA-сертифікати SSL у форматі PEM.

`cipher_algos`

Список допустимих шифрів для використання у SSL-шифруванні.

### Значення, що повертаються

Функція завжди повертає **`true`**. Якщо SSL встановлено некоректно [mysqlirealconnect()](mysqli.real-connect.md) поверне помилку під час спроби підключення.

### Дивіться також

-   [mysqlioptions()](mysqli.options.md) - Встановлення налаштувань
-   [mysqlirealconnect()](mysqli.real-connect.md) - Встановлює з'єднання із сервером mysql
