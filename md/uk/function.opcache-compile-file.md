---
navigation:
  - ref.opcache.md: « Функції OPcache
  - function.opcache-get-configuration.md: opcache\_get\_configuration »
  - index.md: PHP Manual
  - ref.opcache.md: Опції OPcache
title: opcache\_compile\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# opcache\_compile\_file

(PHP 5 >= 5.5.5, PHP 7, PHP 8, PECL ZendOpcache > 7.0.2)

opcache\_compile\_file — Скомпілювати та закешувати, але не виконувати скрипт PHP

### Опис

```methodsynopsis
opcache_compile_file(string $filename): bool
```

Ця функція компілює PHP-скрипт і поміщає його в кеш опкодів, але не запускає його. Ви можете використовувати для прогрівання кеша після перезапуску веб-сервера.

### Список параметрів

`filename`

Шлях до скрипту PHP.

### Значення, що повертаються

Повертає **`true`**, якщо `filename` успішно скомпільований або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо `filename` не може бути завантажений або скомпільований, буде видана помилка рівня **`E_WARNING`**. Для придушення попередження можна використовувати [@](language.operators.errorcontrol.md)

### Дивіться також

-   [opcache\_invalidate()](function.opcache-invalidate.md) \- анулює закешований скрипт
