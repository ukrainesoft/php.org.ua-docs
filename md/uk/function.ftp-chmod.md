---
navigation:
  - function.ftp-chdir.md: « ftpchdir
  - function.ftp-close.md: ftpclose »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftpchmod
---
# ftpchmod

(PHP 5, PHP 7, PHP 8)

ftpchmod — Встановлює права доступу до файлу

### Опис

```methodsynopsis
ftp_chmod(FTP\Connection $ftp, int $permissions, string $filename): int|false
```

Встановлює права доступу до зазначеного видаленого файлу до значення `permissions`

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.md) instance.

`permissions`

Нові права доступу, зазначені у вигляді *восьмеричного* значення.

`filename`

Видалений файл.

### Значення, що повертаються

Повертає нові права доступу до файлу у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **ftpchmod()****

```php
<?php
$file = 'public_html/index.php';

// установка соединения
$ftp = ftp_connect($ftp_server);

// вход с именем пользователя и паролем
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// попытка изменить права доступа к файлу $file на 644
if (ftp_chmod($ftp, 0644, $file) !== false) {
 echo "Права доступа к файлу $file успешно изменены на 644\n";
} else {
 echo "Не удалось изменить права доступа к файлу $file\n";
}

// закрытие соединения
ftp_close($ftp);
?>
```

### Дивіться також

-   [chmod()](function.chmod.md) - Змінює режим доступу до файлу
