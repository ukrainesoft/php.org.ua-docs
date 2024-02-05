---
navigation:
  - function.ftp-rename.md: « ftp\_rename
  - function.ftp-set-option.md: ftp\_set\_option »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_rmdir
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_rmdir

(PHP 4, PHP 5, PHP 7, PHP 8)

ftp\_rmdir - Видаляє директорію

### Опис

```methodsynopsis
ftp_rmdir(FTP\Connection $ftp, string $directory): bool
```

Видаляє директорію `directory`

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`directory`

Ім'я директорії. Параметр повинен мати відносний або абсолютний шлях до порожньої директорії.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**ftp\_rmdir()\*\*\*\*

```php
<?php

$dir = 'www/';

// установка соединения
$ftp = ftp_connect($ftp_server);

// проверка имени пользователя и пароля
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// попытка удаления директории $dir
if (ftp_rmdir($ftp, $dir)) {
    echo "Директория $dir удалена\n";
} else {
    echo "Не удалось удалить директорию $dir\n";
}

ftp_close($ftp);

?>
```

### Дивіться також

-   [ftp\_mkdir()](function.ftp-mkdir.md) \- створює директорію
