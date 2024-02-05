---
navigation:
  - ftp.examples.md: « Приклади
  - ref.ftp.md: Функції FTP »
  - index.md: PHP Manual
  - ftp.examples.md: Приклади
title: Просте використання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Просте використання

**Приклад #1 Приклад використання FTP-функцій**

```php
<?php
// установка соединения
$ftp = ftp_connect($ftp_server);

// вход с именем пользователя и паролем
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// проверка соединения
if ((!$ftp) || (!$login_result)) {
    echo "Не удалось установить соединение с FTP-сервером!";
    echo "Попытка подключения к серверу $ftp_server была произведена под именем $ftp_user_name";
    exit;
} else {
    echo "Установлено соединение с FTP сервером $ftp_server под именем $ftp_user_name";
}

// закачивание файла
$upload = ftp_put($ftp, $destination_file, $source_file, FTP_BINARY);

// проверка результата
if (!$upload) {
    echo "Не удалось закачать файл!";
} else {
    echo "Файл $source_file закачан на $ftp_server под именем $destination_file";
}

// закрытие соединения
ftp_close($conn_id);
?>
```
