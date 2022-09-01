---
navigation:
  - function.session-abort.html: « sessionabort
  - function.session-cache-limiter.html: sessioncachelimiter »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: sessioncacheexpire
---
# sessioncacheexpire

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

sessioncacheexpire — Отримує та/або встановлює термін дії поточного кешу

### Опис

```methodsynopsis
session_cache_expire(?int $value = null): int|false
```

**sessioncacheexpire()** повертає поточне значення налаштування `session.cache_expire`

Термін дії скидається до значення за промовчанням (180), що зберігається в [session.cacheexpire](session.configuration.html#ini.session.cache-expire) під час запиту. Таким чином, потрібно викликати **sessioncacheexpire()** для кожного запиту (і до дзвінка [sessionstart()](function.session-start.md)

### Список параметрів

`value`

Якщо `value` заданий і не дорівнює **`null`**, поточний час життя замінюється на `value`

> **Зауваження**: Налаштування `value` має значення тільки, якщо для `session.cache_limiter` встановлено значення, *відмінне* від `nocache`

### Значення, що повертаються

Повертає поточне налаштування `session.cache_expire`. Значення, що повертається, повинно розглядатися в хвилинах, за замовчуванням - 180. У разі, якщо змінити значення не вдалося, повертається **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `value` може набувати значення **`null`** |

### Приклади

**Приклад #1 Приклад використання **sessioncacheexpire()****

```php
<?php

/* установить ограничитель кеша на 'private' */

session_cache_limiter('private');
$cache_limiter = session_cache_limiter();

/* установить время жизни на 30 минут */
session_cache_expire(30);
$cache_expire = session_cache_expire();

/* старт сессии */

session_start();

echo "Ограничитель кеша теперь равен $cache_limiter<br />";
echo "Закешированные страницы сессии истекают через $cache_expire минут";
?>
```

### Дивіться також

-   [session.cacheexpire](session.configuration.html#ini.session.cache-expire)
-   [session.cachelimiter](session.configuration.html#ini.session.cache-limiter)
-   [sessioncachelimiter()](function.session-cache-limiter.md) - Отримати та/або встановити поточний режим кешування
