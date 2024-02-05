---
navigation:
  - function.ftp-nlist.md: « ftp\_nlist
  - function.ftp-put.md: ftp\_put »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_pasv
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_pasv

(PHP 4, PHP 5, PHP 7, PHP 8)

ftp\_pasv — Вмикає або вимикає пасивний режим

### Опис

```methodsynopsis
ftp_pasv(FTP\Connection $ftp, bool $enable): bool
```

**ftp\_pasv()** вмикає або вимикає пасивний режим. У пасивному режимі передача даних ініціюється клієнтом, а чи не сервером. Цей режим може знадобитися, якщо клієнт перебуває за брандмауером.

Обратите внимание, что**ftp\_pasv()** може бути викликана лише після успішної авторизації, інакше вона завершиться з помилкою.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`enable`

Якщо **`true`**, пасивний режим буде увімкнено, інакше вимкнено.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**ftp\_pasv()\*\*\*\*

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
