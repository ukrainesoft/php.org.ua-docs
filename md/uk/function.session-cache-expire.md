---
navigation:
  - function.session-abort.md: « session\_abort
  - function.session-cache-limiter.md: session\_cache\_limiter »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: session\_cache\_expire
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# session\_cache\_expire

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

session\_cache\_expire — Отримує та/або встановлює термін дії поточного кешу

### Опис

```methodsynopsis
session_cache_expire(?int $value = null): int|false
```

**session\_cache\_expire()** повертає поточне значення налаштування `session.cache_expire`

Термін дії скидається до значення за промовчанням (180), що зберігається в [session.cache\_expire](session.configuration.md#ini.session.cache-expire) під час запиту. Таким чином, потрібно викликати **session\_cache\_expire()** для кожного запиту (і до дзвінка [session\_start()](function.session-start.md)

### Список параметрів

`value`

Якщо `value` заданий і не дорівнює **`null`**, текущее время жизни заменяется на`value`

> **Зауваження**: Настройка`value` має значення тільки, якщо для `session.cache_limiter`установлено значение,*відмінне*от`nocache`

### Значення, що повертаються

Повертає поточне налаштування `session.cache_expire`. Значення, що повертається, повинно розглядатися в хвилинах, за замовчуванням - 180. У разі, якщо змінити значення не вдалося, повертається **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `value` може набувати значення **`null`** |

### Приклади

**Пример #1 Пример использования**session\_cache\_expire()\*\*\*\*

```php
<?php

/* установить ограничитель кеша на 'private' */

session_cache_limiter('private');
$cache_limiter = session_cache_limiter();

/* установить время жизни на 30 минут */
session_cache_expire(30);
$cache_expire = session_cache_expire();

/* старт сессии */

session_start();

echo "Ограничитель кеша теперь равен $cache_limiter<br />";
echo "Закешированные страницы сессии истекают через $cache_expire минут";
?>
```

### Дивіться також

-   [session.cache\_expire](session.configuration.md#ini.session.cache-expire)
-   [session.cache\_limiter](session.configuration.md#ini.session.cache-limiter)
-   [session\_cache\_limiter()](function.session-cache-limiter.md) \- Отримати та/або встановити поточний режим кешування
