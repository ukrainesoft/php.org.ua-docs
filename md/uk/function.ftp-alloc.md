---
navigation:
  - ref.ftp.md: « Функції FTP
  - function.ftp-append.md: ftp\_append »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_alloc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_alloc

(PHP 5, PHP 7, PHP 8)

ftp\_alloc — Резервує місце на диску для закачуваного файлу

### Опис

```methodsynopsis
ftp_alloc(FTP\Connection $ftp, int $size, string &$response = null): bool
```

Надсилає команду `ALLO` FTP-серверу для резервування місця під файл, що завантажується.

> **Зауваження** :
> 
> Багато FTP-серверів не підтримують цю команду. Такі сервери повертають код невдачі (**`false`**), що означає відсутність підтримки цієї команди, або код успішного виконання (**`true`**), що означає, що в резервуванні немає необхідності і клієнту слід продовжувати, ніби операція була успішно виконана. Тому цю функцію слід використовувати з серверами, які потребують обов'язкового резервування.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`size`

Кількість байт, що резервуються.

`response`

Текстове подання відповіді сервера буде повернуто за посиланням у аргумент `response`якщо він вказаний.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**ftp\_alloc()\*\*\*\*

```php
<?php

$file = "/home/user/myfile";

/* соединение с сервером */
$ftp = ftp_connect('ftp.example.com');
$login_result = ftp_login($ftp, 'anonymous', 'user@example.com');

if (ftp_alloc($ftp, filesize($file), $result)) {
  echo "Место на сервере успешно зарезервировано.  Отправляю $file.\n";
  ftp_put($conn_id, '/incoming/myfile', $file, FTP_BINARY);
} else {
  echo "Не удалось зарезервировать место на сервере. Ответ сервера: $result\n";
}

ftp_close($ftp);

?>
```

### Дивіться також

-   [ftp\_put()](function.ftp-put.md) \- Завантажує файл на FTP-сервер
-   [ftp\_fput()](function.ftp-fput.md) \- Завантажує попередньо відкритий файл на FTP-сервер
