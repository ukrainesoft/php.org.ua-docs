---
navigation:
  - function.ftp-nlist.md: « ftpnlist
  - function.ftp-put.md: ftpput »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftppasv
---
# ftppasv

(PHP 4, PHP 5, PHP 7, PHP 8)

ftppasv — Вмикає або вимикає пасивний режим

### Опис

```methodsynopsis
ftp_pasv(FTP\Connection $ftp, bool $enable): bool
```

**ftppasv()** вмикає або вимикає пасивний режим. У пасивному режимі передача даних ініціюється клієнтом, а чи не сервером. Цей режим може знадобитися, якщо клієнт перебуває за брандмауером.

Зверніть увагу, що **ftppasv()** може бути викликана лише після успішної авторизації, інакше вона завершиться з помилкою.

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.md) instance.

`enable`

Якщо **`true`**, пасивний режим буде увімкнено, інакше вимкнено.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **ftppasv()****

```php
<?php
$file = 'somefile.txt';
$remote_file = 'readme.txt';

// установка соединения
$conn_id = ftp_connect($ftp_server);

// проверка имени пользователя и пароля
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// включение пассивного режима
ftp_pasv($conn_id, true);

// загрузка файла
if (ftp_put($conn_id, $remote_file, $file, FTP_ASCII)) {
 echo "$file успешно загружен на сервер\n";
} else {
 echo "Не удалось загрузить $file на сервер\n";
}

// закрытие соединения
ftp_close($conn_id);
?>
```
