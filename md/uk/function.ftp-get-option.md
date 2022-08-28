Отримує поточні параметри FTP-з'єднання

-   [« ftp\_fput](function.ftp-fput.html)
    
-   [ftp\_get »](function.ftp-get.html)
    
-   [PHP Manual](index.html)
    
-   [Функции FTP](ref.ftp.html)
    
-   Отримує поточні параметри FTP-з'єднання
    

# ftpgetoption

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

ftpgetoption — Отримує поточні параметри FTP-з'єднання.

### Опис

```methodsynopsis
ftp_get_option(FTP\Connection $ftp, int $option): int|bool
```

Ця функція повертає значення запитаної опції `option` для зазначеного FTP-з'єднання.

### Список параметрів

`ftp`

Ан [FTP\\Connection](class.ftp-connection.html) instance.

`option`

На даний момент підтримуються такі опції:

<table class="doctable table"><caption><strong>Підтримувані поточні опції FTP</strong></caption><tbody class="tbody"><tr><td><strong><code>FTP_TIMEOUT_SEC</code></strong></td><td>Повертає поточний час очікування, що використовується в мережевих операціях.</td></tr><tr><td><strong><code>FTP_AUTOSEEK</code></strong></td><td>Повертає <strong><code>true</code></strong>, якщо цю опцію увімкнено, інакше <strong><code>false</code></strong>.. td&gt;</td></tr></tbody></table>

### Значення, що повертаються

Повертає значення у разі успішного виконання, або **`false`**, якщо вказана опція `option` не підтримується. У разі також викликається попередження.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **ftpgetoption()****

```php
<?php
// Получаем время ожидания соединения
$timeout = ftp_get_option($ftp, FTP_TIMEOUT_SEC);
?>
```

### Дивіться також

-   [ftp\_set\_option()](function.ftp-set-option.html) - Встановлює параметри з'єднання з FTP-сервером