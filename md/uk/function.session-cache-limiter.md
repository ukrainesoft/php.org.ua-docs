---
navigation:
  - function.session-cache-expire.md: « session\_cache\_expire
  - function.session-commit.md: session\_commit »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: session\_cache\_limiter
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# session\_cache\_limiter

(PHP 4 >= 4.0.3, PHP 5, PHP 7, PHP 8)

session\_cache\_limiter — Отримати та/або встановити поточний режим кешування

### Опис

```methodsynopsis
session_cache_limiter(?string $value = null): string|false
```

**session\_cache\_limiter()** повертає ім'я поточного кешування.

Режим кешування визначає, які HTTP-заголовки керування кешем надсилати клієнту. Ці заголовки визначають, якими правилами кешування контенту повинні керуватися клієнт та проміжні проксі. Встановлення обмежувача на значення `nocache`запрещает любое кеширование. Значение`public` дозволяє кешування як на стороні клієнта, так і на проксі-серверах . `private`запрещает кеширование прокси-серверам, но разрешает клиенту.

Якщо в режимі `private` надіслати заголовок Expire, то це може привести деякі браузери, включаючи Mozilla, в замішання. Ви можете обійти цю проблему, використовуючи режим `private_no_expire`. У цьому режимі заголовок `Expire`никогда не будет послан.

Установка режима кеширования в`''` відключає автоматичне надсилання кеш-заголовків.

Під час початку запиту режим кешування скидається до значення за промовчанням, яке зберігається в [session.cache\_limiter](session.configuration.md#ini.session.cache-limiter). Таким чином, вам необхідно викликати **session\_cache\_limiter()** для кожного запиту (перед тим, як викликана функція [session\_start()](function.session-start.md)

### Список параметрів

`value`

Якщо `value` вказаний і не дорівнює **`null`**, ім'я поточного кешування змінюється на нове значення.

**Можливі значення**

| Значение | Посылаемый заголовок |
| --- | --- |
| `public` |  |
| Expires: (коли в майбутньому, залежно від session.cache\_expire) |  |
| Cache-Control: public, max-age=(колись у майбутньому, залежно від session.cache\_expire) |  |
| Last-Modified: (тимчасова мітка останнього збереження сесії) |  |

`private_no_expire`

Cache-Control: private, max-age=(session.cache\_expire у майбутньому), pre-check=(session.cache\_expire у майбутньому) Last-Modified: (тимчасова мітка останнього збереження сесії)

`private`

Expires: Thu, 19 Nov 1981 08:52:00 GMT Cache-Control: private, max-age=(session.cache\_expire у майбутньому), pre-check=(session.cache\_expire у майбутньому) Last-Modified: (тимчасова мітка останнього збереження сесії)

`nocache`

Expires: Thu, 19 Nov 1981 08:52:00 GMT Cache-Control: no-store, no-cache, must-revalidate, post-check=0, pre-check=0 Pragma: no-cache

### Значення, що повертаються

Повертає назву поточного режиму кешування. Якщо змінити значення не вдалося, повертається **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `value` може набувати значення **`null`** |

### Приклади

**Приклад #1 Приклад використання** session\_cache\_limiter()\*\*\*\*

```php
<?php

/* установить режим кеширования на 'private' */

session_cache_limiter('private');
$cache_limiter = session_cache_limiter();

echo "Режим кеширования установлен в $cache_limiter<br />";
?>
```

### Дивіться також

-   [session.cache\_limiter](session.configuration.md#ini.session.cache-limiter)
