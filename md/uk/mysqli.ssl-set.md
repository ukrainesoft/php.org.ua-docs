---
navigation:
  - mysqli.sqlstate.md: '« mysqli::$sqlstate'
  - mysqli.stat.md: 'mysqli::stat »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::ssl\_set'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::ssl\_set

# mysqli\_ssl\_set

(PHP 5, PHP 7, PHP 8)

mysqli::ssl\_set -- mysqli\_ssl\_set — Використовується для встановлення безпечних з'єднань за допомогою SSL

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::ssl_set(    ?string $key,    ?string $certificate,    ?string $ca_certificate,    ?string $ca_path,    ?string $cipher_algos): true
```

Процедурний стиль

```methodsynopsis
mysqli_ssl_set(    mysqli $mysql,    ?string $key,    ?string $certificate,    ?string $ca_certificate,    ?string $ca_path,    ?string $cipher_algos): true
```

Використовується для встановлення безпечних з'єднань за допомогою SSL. Функцію необхідно викликати до дзвінка [mysqli\_real\_connect()](mysqli.real-connect.md). Для роботи функції потрібно включити підтримку OpenSSL, інакше функція робити нічого не буде.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

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

Функція завжди повертає \*\*`true`\*\*Если SSL установлен некорректно[mysqli\_real\_connect()](mysqli.real-connect.md) поверне помилку під час спроби підключення.

### Дивіться також

-   [mysqli\_options()](mysqli.options.md) \- Встановлення налаштувань
-   [mysqli\_real\_connect()](mysqli.real-connect.md) \- Встановлює з'єднання із сервером mysql
