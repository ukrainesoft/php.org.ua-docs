---
navigation:
  - function.ftp-cdup.md: « ftpcdup
  - function.ftp-chmod.md: ftpchmod »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftpchdir
---
# ftpchdir

(PHP 4, PHP 5, PHP 7, PHP 8)

ftpchdir — Змінює поточну директорію на FTP-сервері

### Опис

```methodsynopsis
ftp_chdir(FTP\Connection $ftp, string $directory): bool
```

Змінює поточну директорію на задану аргументом.

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.md) instance.

`directory`

Цільова директорія.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо зміна директорії завершилася невдачею, PHP викликає попередження.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **ftpchdir()****

```php
<?php

// установка соединения
$ftp = ftp_connect($ftp_server);

// вход с именем пользователя и паролем
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// проверка соединения
if ((!$ftp) || (!$login_result)) {
    die("Не удалось подключиться к FTP-серверу!");
}

echo "Текущая директория: " . ftp_pwd($ftp) . "\n";

// пытаемся сменить текущую директорию на somedir
if (ftp_chdir($ftp, "somedir")) {
    echo "Новая текущая директория: " . ftp_pwd($ftp) . "\n";
} else {
    echo "Не удалось сменить директорию\n";
}

// закрытие соединения
ftp_close($ftp);
?>
```

### Дивіться також

-   [ftpcdup()](function.ftp-cdup.md) - Переходить до батьківської директорії
-   [ftppwd()](function.ftp-pwd.md) - Повертає ім'я поточної директорії
