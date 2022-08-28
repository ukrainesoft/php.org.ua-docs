Доступ до URL-адрес за протоколом HTTP(s)

-   [« file://](wrappers.file.html)
    
-   [ftp:// »](wrappers.ftp.html)
    
-   [PHP Manual](index.html)
    
-   [Поддерживаемые протоколы и обёртки](wrappers.html)
    
-   Доступ до URL-адрес за протоколом HTTP(s)
    

# http://

# https://

http:// -- https:// — Доступ до URL-адрес за протоколом HTTP(s)

### Опис

Надає доступ лише для читання файлів/ресурсів через HTTP. За промовчанням використовується HTTP 1.0 GET. Для підтримки віртуальних хостів на основі імен разом із запитом надсилається заголовок `Host:`. Якщо ви налаштували рядок [user\_agent](filesystem.configuration.html#ini.user-agent), використовуючи ваш файл php.ini або контекст потоку, вона також буде включена в запит.

Цей потік також дозволяє отримати доступ до *вмісту* ресурсу; заголовки зберігаються у змінній [$http\_response\_header](reserved.variables.httpresponseheader.html)

Якщо важливо знати URL, з якого було отримано документ (після всіх переадресацій, які були зроблені), вам необхідно обробити серію заголовків відповідей, що повертаються потоком.

INI-директива [from](filesystem.configuration.html#ini.from) буде використовуватися для заголовка `From:`, якщо встановлена ​​та не перевизначена в контексті [Контекстные опции и параметры](context.html)

### Використання

-   [http://example.com](http://example.com)
-   [http://example.com/file.php?var1=val1&var2=val2](http://example.com/file.php?var1=val1&var2=val2)
-   [http://user:password@example.com](http://user:password@example.com)
-   [https://example.com](https://example.com)
-   [https://example.com/file.php?var1=val1&var2=val2](https://example.com/file.php?var1=val1&var2=val2)
-   [https://user:password@example.com](https://user:password@example.com)

### Опції

**Основна інформація**

| Атрибут | Поддержка |
| --- | --- |
| Обмеження по [allow\_url\_fopen](filesystem.configuration.html#ini.allow-url-fopen) | Так |
| Читання | Так |
| Запис | Ні |
| Додавання | Ні |
| Одночасне читання та запис | Недоступно |
| Підтримка [stat()](function.stat.html) | Ні |
| Підтримка [unlink()](function.unlink.html) | Ні |
| Підтримка [rename()](function.rename.html) | Ні |
| Підтримка [mkdir()](function.mkdir.html) | Ні |
| Підтримка [rmdir()](function.rmdir.html) | Ні |

### Приклади

**Приклад #1 Визначення URL, з якого було забрано документ після переадресації**

```php
<?php
$url = 'http://www.example.com/redirecting_page.php';

$fp = fopen($url, 'r');

$meta_data = stream_get_meta_data($fp);
foreach ($meta_data['wrapper_data'] as $response) {

    /* Были ли мы переадресованы? */
    if (strtolower(substr($response, 0, 10)) == 'location: ') {

        /* Сохранить в $url адрес, куда нас переадресовали */
        $url = substr($response, 10);
    }

}

?>
```

### Примітки

> **Зауваження**: Протокол HTTPS підтримується лише коли модуль [openssl](book.openssl.html) включений.

З'єднання HTTP призначені лише для читання; запис даних або копіювання файлів у HTTP-ресурс не підтримується.

Надсилання запитів *POST* і *PUT*, наприклад, може бути виконана за допомогою [HTTP-контекста](context.http.html)

### Дивіться також

-   [Опции контекста HTTP](context.http.html)
-   [$http\_response\_header](reserved.variables.httpresponseheader.html)
-   [stream\_get\_meta\_data()](function.stream-get-meta-data.html) - Витягує заголовок/метадані з потоків/файлових покажчиків