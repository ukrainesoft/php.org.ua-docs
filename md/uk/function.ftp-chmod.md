---
navigation:
  - function.ftp-chdir.md: « ftp\_chdir
  - function.ftp-close.md: ftp\_close »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_chmod
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_chmod

(PHP 5, PHP 7, PHP 8)

ftp\_chmod — Встановлює права доступу до файлу

### Опис

```methodsynopsis
ftp_chmod(FTP\Connection $ftp, int $permissions, string $filename): int|false
```

Встановлює права доступу до зазначеного видаленого файлу до значення `permissions`

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`permissions`

Нові права доступу, зазначені у вигляді *восьмеричного*значения.

`filename`

Видалений файл.

### Значення, що повертаються

Повертає нові права доступу до файлу у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**ftp\_chmod()\*\*\*\*

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

-   [chmod()](function.chmod.md) \- Змінює режим доступу до файлу
