Отримати та/або встановити поточний режим кешування

-   [« session\_cache\_expire](function.session-cache-expire.html)
    
-   [session\_commit »](function.session-commit.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с сессиями](ref.session.html)
    
-   Отримати та/або встановити поточний режим кешування
    

# sessioncachelimiter

(PHP 4> = 4.0.3, PHP 5, PHP 7, PHP 8)

sessioncachelimiter — Отримати та/або встановити поточний режим кешування

### Опис

```methodsynopsis
session_cache_limiter(?string $value = null): string|false
```

**sessioncachelimiter()** повертає назву поточного режиму кешування.

Режим кешування визначає, які HTTP-заголовки керування кешем надсилати клієнту. Ці заголовки визначають, якими правилами кешування контенту повинні керуватися клієнт та проміжні проксі. Встановлення обмежувача на значення `nocache` забороняє будь-яке кешування. Значення `public` дозволяє кешування як на стороні клієнта, так і на проксі-серверах . `private` забороняє кешування проксі-серверам, але дозволяє клієнту.

Якщо в режимі `private` надіслати заголовок Expire, то це може привести деякі браузери, включаючи Mozilla, в замішання. Ви можете обійти цю проблему, використовуючи режим `private_no_expire`. У цьому режимі заголовок `Expire` ніколи не буде посланий.

Встановлення режиму кешування в `''` відключає автоматичне надсилання кеш-заголовків.

Під час початку запиту режим кешування скидається до значення за промовчанням, яке зберігається в [session.cache\_limiter](session.configuration.html#ini.session.cache-limiter). Таким чином, вам необхідно викликати **sessioncachelimiter()** для кожного запиту (перед тим, як викликана функція [session\_start()](function.session-start.html)

### Список параметрів

`value`

Якщо `value` вказаний і не дорівнює **`null`**, ім'я поточного кешування змінюється на нове значення.

**Можливі значення**

| Значение                                                                               | Посылаемый заголовок |
|----------------------------------------------------------------------------------------|----------------------|
| `public`                                                                               |                      |
| Expires: (коли в майбутньому, залежно від session.cacheexpire)                         |                      |
| Cache-Control: public, max-age=(колись у майбутньому, залежно від session.cacheexpire) |                      |
| Last-Modified: (тимчасова мітка останнього збереження сесії)                           |                      |

`private_no_expire`

Cache-Control: private, max-age=(session.cacheexpire у майбутньому), pre-check=(session.cacheexpire у майбутньому) Last-Modified: (тимчасова мітка останнього збереження сесії)

`private`

Expires: Thu, 19 Nov 1981 08:52:00 GMT Cache-Control: private, max-age=(session.cacheexpire у майбутньому), pre-check=(session.cacheexpire у майбутньому) Last-Modified: (тимчасова мітка останнього збереження сесії)

`nocache`

Expires: Thu, 19 Nov 1981 08:52:00 GMT Cache-Control: no-store, no-cache, must-revalidate, post-check=0, pre-check=0 Pragma: no-cache

### Значення, що повертаються

Повертає назву поточного режиму кешування. Якщо змінити значення не вдалося, повертається **`false`**

### список змін

| Версия | Описание                                  |
|--------|-------------------------------------------|
|        | `value` може набувати значення **`null`** |

### Приклади

**Приклад #1 Приклад використання **sessioncachelimiter()****

```php
<?php

/* установить режим кеширования на 'private' */

session_cache_limiter('private');
$cache_limiter = session_cache_limiter();

echo "Режим кеширования установлен в $cache_limiter<br />";
?>
```

### Дивіться також

-   [session.cache\_limiter](session.configuration.html#ini.session.cache-limiter)