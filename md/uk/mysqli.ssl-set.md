Використовується для встановлення безпечних з'єднань за допомогою SSL

-   [« mysqli::$sqlstate](mysqli.sqlstate.html)
    
-   [mysqli::stat »](mysqli.stat.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Використовується для встановлення безпечних з'єднань за допомогою SSL
    

# mysqli::sslset

# mysqlisslset

(PHP 5, PHP 7, PHP 8)

mysqli::sslset - mysqlisslset — Використовується для встановлення безпечних з'єднань за допомогою SSL

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::ssl_set(    ?string $key,    ?string $certificate,    ?string $ca_certificate,    ?string $ca_path,    ?string $cipher_algos): bool
```

Процедурний стиль

```methodsynopsis
mysqli_ssl_set(    mysqli $mysql,    ?string $key,    ?string $certificate,    ?string $ca_certificate,    ?string $ca_path,    ?string $cipher_algos): bool
```

Використовується для встановлення безпечних з'єднань за допомогою SSL. Функцію необхідно викликати до дзвінка [mysqli\_real\_connect()](mysqli.real-connect.html). Для роботи функції потрібно включити підтримку OpenSSL, інакше функція робити нічого не буде.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqli\_connect()](function.mysqli-connect.html) або [mysqli\_init()](mysqli.init.html)

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

Функція завжди повертає **`true`**. Якщо SSL встановлено некоректно [mysqli\_real\_connect()](mysqli.real-connect.html) поверне помилку під час спроби підключення.

### Дивіться також

-   [mysqli\_options()](mysqli.options.html) - Встановлення налаштувань
-   [mysqli\_real\_connect()](mysqli.real-connect.html) - Встановлює з'єднання із сервером mysql