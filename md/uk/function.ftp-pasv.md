Вмикає або вимикає пасивний режим

-   [« ftp\_nlist](function.ftp-nlist.html)
    
-   [ftp\_put »](function.ftp-put.html)
    
-   [PHP Manual](index.html)
    
-   [Функции FTP](ref.ftp.html)
    
-   Вмикає або вимикає пасивний режим
    

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

Ан [FTP\\Connection](class.ftp-connection.html) instance.

`enable`

Якщо **`true`**, пасивний режим буде увімкнено, інакше вимкнено.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                              |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **ftppasv()****

```php
<?php
$file = 'somefile.txt';
$remote_file = 'readme.txt';

// установка соединения
$conn_id = ftp_connect($ftp_server);

// проверка имени пользователя и пароля
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// включение пассивного режима
ftp_pasv($conn_id, true);

// загрузка файла
if (ftp_put($conn_id, $remote_file, $file, FTP_ASCII)) {
 echo "$file успешно загружен на сервер\n";
} else {
 echo "Не удалось загрузить $file на сервер\n";
}

// закрытие соединения
ftp_close($conn_id);
?>
```