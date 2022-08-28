Callback-функція для параметра контексту notification

-   [« stream\_isatty](function.stream-isatty.html)
    
-   [stream\_register\_wrapper »](function.stream-register-wrapper.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с потоками](ref.stream.html)
    
-   Callback-функція для параметра контексту notification
    

# streamnotificationcallback

(PHP 5> = 5.2.0, PHP 7, PHP 8)

streamnotificationcallback - Callback-функція для параметра контексту `notification`

### Опис

```methodsynopsis
stream_notification_callback(    int $notification_code,    int $severity,    string $message,    int $message_code,    int $bytes_transferred,    int $bytes_max): void
```

Callback-функція типу [callable](language.types.callable.html), що використовується [параметром контекста notification](context.params.html#context.params.notification), що викликається під час події.

> **Зауваження**
> 
> Це *не* справжня функція, лише прототип того, як має бути реалізована функція.

### Список параметрів

`notification_code`

Одна з констант оповіщення **`STREAM_NOTIFY_*`**

`severity`

Одна з констант оповіщення **`STREAM_NOTIFY_SEVERITY_*`**

`message`

Передається, якщо для події доступне описове повідомлення.

`message_code`

Передається, якщо для події доступний код повідомлення, що описує.

Значення даної величини залежить від використовуваної обгортки.

`bytes_transferred`

Якщо доступно, то параметр `bytes_transferred` буде заповнено.

`bytes_max`

Якщо доступно, то параметр `bytes_max` буде заповнено.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **streamnotificationcallback()****

```php
<?php
function stream_notification_callback($notification_code, $severity, $message, $message_code, $bytes_transferred, $bytes_max) {

    switch($notification_code) {
        case STREAM_NOTIFY_RESOLVE:
        case STREAM_NOTIFY_AUTH_REQUIRED:
        case STREAM_NOTIFY_COMPLETED:
        case STREAM_NOTIFY_FAILURE:
        case STREAM_NOTIFY_AUTH_RESULT:
            var_dump($notification_code, $severity, $message, $message_code, $bytes_transferred, $bytes_max);
            /* Игнорируем */
            break;

        case STREAM_NOTIFY_REDIRECTED:
            echo "Перенаправлены на: ", $message;
            break;

        case STREAM_NOTIFY_CONNECT:
            echo "Подсоединились...";
            break;

        case STREAM_NOTIFY_FILE_SIZE_IS:
            echo "Получили размер файла: ", $bytes_max;
            break;

        case STREAM_NOTIFY_MIME_TYPE_IS:
            echo "Получили mime-тип файла: ", $message;
            break;

        case STREAM_NOTIFY_PROGRESS:
            echo "Пошёл прогресс, пока загружено ", $bytes_transferred, " байт";
            break;
    }
    echo "\n";
}

$ctx = stream_context_create();
stream_context_set_params($ctx, array("notification" => "stream_notification_callback"));

file_get_contents("http://php.net/contact", false, $ctx);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Подсоединились...
Получили mime-тип файла: text/html; charset=utf-8
Перенаправлены на: http://no.php.net/contact
Подсоединились...
Получили размер файла: 0
Получили mime-тип файла: text/html; charset=utf-8
Перенаправлены на: http://no.php.net/contact.php
Подсоединились...
Получили размер файла: 4589
Получили mime-тип файла: text/html;charset=utf-8
Пошёл прогресс, пока загружено 0 байт
Пошёл прогресс, пока загружено 0 байт
Пошёл прогресс, пока загружено 0 байт
Пошёл прогресс, пока загружено 1440 байт
Пошёл прогресс, пока загружено 2880 байт
Пошёл прогресс, пока загружено 4320 байт
Пошёл прогресс, пока загружено 5760 байт
Пошёл прогресс, пока загружено 6381 байт
Пошёл прогресс, пока загружено 7002 байт
```

**Приклад #2 Простий індикатор для завантажувача файлів із командного рядка**

```php
<?php
function usage($argv) {
    echo "Использование:\n";
    printf("\tphp %s <http://example.com/file> <localfile>\n", $argv[0]);
    exit(1);
}

function stream_notification_callback($notification_code, $severity, $message, $message_code, $bytes_transferred, $bytes_max) {
    static $filesize = null;

    switch($notification_code) {
    case STREAM_NOTIFY_RESOLVE:
    case STREAM_NOTIFY_AUTH_REQUIRED:
    case STREAM_NOTIFY_COMPLETED:
    case STREAM_NOTIFY_FAILURE:
    case STREAM_NOTIFY_AUTH_RESULT:
        /* Игнорируем */
        break;

    case STREAM_NOTIFY_REDIRECTED:
        echo "Перенаправлены на: ", $message, "\n";
        break;

    case STREAM_NOTIFY_CONNECT:
        echo "Подсоединились...\n";
        break;

    case STREAM_NOTIFY_FILE_SIZE_IS:
        $filesize = $bytes_max;
        echo "Размер файла: ", $filesize, "\n";
        break;

    case STREAM_NOTIFY_MIME_TYPE_IS:
        echo "Mime-тип файла: ", $message, "\n";
        break;

    case STREAM_NOTIFY_PROGRESS:
        if ($bytes_transferred > 0) {
            if (!isset($filesize)) {
                printf("\rНеизвестный размер файла.. Закачано %2d Кб..", $bytes_transferred/1024);
            } else {
                $length = (int)(($bytes_transferred/$filesize)*100);
                printf("\r[%-100s] %d%% (%2d/%2d kb)", str_repeat("=", $length). ">", $length, ($bytes_transferred/1024), $filesize/1024);
            }
        }
        break;
    }
}

isset($argv[1], $argv[2]) or usage($argv);

$ctx = stream_context_create();
stream_context_set_params($ctx, array("notification" => "stream_notification_callback"));

$fp = fopen($argv[1], "r", false, $ctx);
if (is_resource($fp) && file_put_contents($argv[2], $fp)) {
    echo "\nГотово!\n";
    exit(0);
}

$err = error_get_last();
echo "\nОшшшшибкка..\n", $err["message"], "\n";
exit(1);
?>
```

Виконання вищенаведеного прикладу з наступними опціями: `php -n fetch.php http://no2.php.net/get/php-5-LATEST.tar.bz2/from/this/mirror php-latest.tar.bz2` виведе щось схоже на це:

```
Подсоединились...
Mime-тип файла: text/html; charset=utf-8
Перенаправлены на: http://no2.php.net/distributions/php-5.2.5.tar.bz2
Подсоединились...
Размер файла: 7773024
Mime-тип файла: application/octet-stream
[========================================>                                                           ] 40% (3076/7590 kb)
```

### Дивіться також

-   [Параметры контекста](context.params.html)