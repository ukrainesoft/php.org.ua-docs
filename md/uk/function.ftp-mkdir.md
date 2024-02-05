---
navigation:
  - function.ftp-mdtm.md: « ftp\_mdtm
  - function.ftp-mlsd.md: ftp\_mlsd »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_mkdir
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_mkdir

(PHP 4, PHP 5, PHP 7, PHP 8)

ftp\_mkdir - Створює директорію

### Опис

```methodsynopsis
ftp_mkdir(FTP\Connection $ftp, string $directory): string|false
```

Створює директорію `directory` на FTP-сервері.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`directory`

Ім'я директорії, що створюється.

### Значення, що повертаються

Повертає ім'я щойно створеної директорії у разі успішного виконання або **`false`** в іншому випадку.

### Помилки

Видає помилку рівня **`E_WARNING`**, якщо каталог вже існує або відповідні права доступу перешкоджають створенню каталогу.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**ftp\_mkdir()\*\*\*\*

```php
<?php

$dir = 'www';

// установка соединения
$ftp = ftp_connect($ftp_server);

// вход с именем пользователя и паролем
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// попытка создания директории $dir
if (ftp_mkdir($ftp, $dir)) {
 echo "Создана директория $dir\n";
} else {
 echo "Не удалось создать директорию $dir\n";
}

// закрытие соединения
ftp_close($ftp);
?>
```

### Дивіться також

-   [ftp\_rmdir()](function.ftp-rmdir.md) \- видаляє директорію
