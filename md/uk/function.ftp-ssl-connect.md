---
navigation:
  - function.ftp-size.md: « ftp\_size
  - function.ftp-systype.md: ftp\_systype »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_ssl\_connect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_ssl\_connect

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

ftp\_ssl\_connect — Встановлює з'єднання з FTP-сервером через SSL

### Опис

```methodsynopsis
ftp_ssl_connect(string $hostname, int $port = 21, int $timeout = 90): FTP\Connection|false
```

\*\*ftp\_ssl\_connect()\**устанавливает*явне\* SSL з'єднання з FTP-сервером, заданим аргументом `hostname`. Це означає, що **ftp\_ssl\_connect()** буде успішним навіть якщо сервер не налаштований для SSL-FTP, або його сертифікат недійсний. Тільки коли буде викликано функцію [ftp\_login()](function.ftp-login.md), клієнт надішле необхідну команду AUTH FTP, так що у зазначених випадках [ftp\_login()](function.ftp-login.md) завершиться помилкою.

> **Зауваження** **Чому ця функція може бути не визначена**
> 
> До PHP 7.0.0**ftp\_ssl\_connect()** була доступна тільки якщо PHP був зібраний з підтримкою [OpenSSL](ref.openssl.md); це означає, що у Windows ця функція не була визначена в офіційних збірках PHP. Щоб використовувати цю функцію під Windows, вам доведеться зібрати PHP самостійно, щоб увімкнути підтримку OpenSSL.

> **Зауваження** :
> 
> \*\*ftp\_ssl\_connect()\*\*не предназначена для использования по протоколу sFTP. Для использования sFTP из PHP смотрите функцию[ssh2\_sftp()](function.ssh2-sftp.md)

### Список параметрів

`hostname`

Адреса FTP-сервера. Цей параметр не повинен містити сліші в кінці та префікс `ftp://`в начале.

`port`

Задає порт, у якому встановлюється з'єднання. Якщо дорівнює нулю або опущений, використовується стандартний для протоколу FTP - порт 21.

`timeout`

Задає час очікування для всіх операцій із цим з'єднанням. За замовчуванням час очікування встановлюється за 90 секунд. Отримати та встановити значення часу очікування можна також за допомогою функцій [ftp\_set\_option()](function.ftp-set-option.md) і [ftp\_get\_option()](function.ftp-get-option.md)

### Значення, що повертаються

Повертає [FTP\\Connection](class.ftp-connection.md) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Повертає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше повертався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання функції** ftp\_ssl\_connect()\*\*\*\*

```php
<?php

// установка ssl-соединения
$ftp = ftp_ssl_connect($ftp_server);

// проверка имени пользователя и пароля
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

if (!$login_result) {
    // В этом случае PHP уже выбросил сообщение уровня E_WARNING
    die("can't login");
}

echo ftp_pwd($ftp); // /

// закрытие ssl-соединения
ftp_close($ftp);
?>
```

### Дивіться також

-   [ftp\_connect()](function.ftp-connect.md) \- Встановлює з'єднання з FTP-сервером
