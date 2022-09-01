---
navigation:
  - wrappers.file.md: '« file://'
  - wrappers.ftp.md: 'ftp:// »'
  - index.md: PHP Manual
  - wrappers.md: Підтримувані протоколи та обгортки
title: 'http://'
---
# http://

# https://

http:// -- https:// — Доступ до URL-адрес за протоколом HTTP(s)

### Опис

Надає доступ лише для читання файлів/ресурсів через HTTP. За промовчанням використовується HTTP 1.0 GET. Для підтримки віртуальних хостів на основі імен разом із запитом надсилається заголовок `Host:`. Якщо ви налаштували рядок [useragent](filesystem.configuration.html#ini.user-agent), використовуючи ваш файл php.ini або контекст потоку, вона також буде включена в запит.

Цей потік також дозволяє отримати доступ до *вмісту* ресурсу; заголовки зберігаються у змінній [$httpresponseheader](reserved.variables.httpresponseheader.md)

Якщо важливо знати URL, з якого було отримано документ (після всіх переадресацій, які були зроблені), вам необхідно обробити серію заголовків відповідей, що повертаються потоком.

INI-директива [from](filesystem.configuration.html#ini.from) буде використовуватися для заголовка `From:`, якщо встановлена ​​та не перевизначена в контексті [Контекстні опції та параметри](context.md)

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
| Обмеження по [allowurlfopen](filesystem.configuration.html#ini.allow-url-fopen) | Так |
| Читання | Так |
| Запис | Ні |
| Додавання | Ні |
| Одночасне читання та запис | Недоступно |
| Підтримка [stat()](function.stat.md) | Ні |
| Підтримка [unlink()](function.unlink.md) | Ні |
| Підтримка [rename()](function.rename.md) | Ні |
| Підтримка [mkdir()](function.mkdir.md) | Ні |
| Підтримка [rmdir()](function.rmdir.md) | Ні |

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

> **Зауваження**: Протокол HTTPS підтримується лише коли модуль [openssl](book.openssl.md) включений.

З'єднання HTTP призначені лише для читання; запис даних або копіювання файлів у HTTP-ресурс не підтримується.

Надсилання запитів *POST* і *PUT*, наприклад, може бути виконана за допомогою [HTTP-контекста](context.http.md)

### Дивіться також

-   [Опции контекста HTTP](context.http.md)
-   [$httpresponseheader](reserved.variables.httpresponseheader.md)
-   [streamgetmetadata()](function.stream-get-meta-data.html) - Витягує заголовок/метадані з потоків/файлових покажчиків
