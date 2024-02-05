---
navigation:
  - function.opcache-is-script-cached.md: « opcache\_is\_script\_cached
  - book.outcontrol.md: Контроль виведення »
  - index.md: PHP Manual
  - ref.opcache.md: Опції OPcache
title: opcache\_reset
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# opcache\_reset

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL ZendOpcache >= 7.0.0)

opcache\_reset — Скидає вміст кешу опкодів

### Опис

```methodsynopsis
opcache_reset(): bool
```

Функція скидає весь кеш. Після виклику **opcache\_reset()** всі скрипти будуть заново завантажені, скомпільовані та поміщені в кеш після їхнього наступного виклику. Функція скидає лише кеш у пам'яті, не торкаючись файлового кешу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо кеш опкодів був скинутий або **`false`**, якщо кеш вимкнено, очікується перезапуск або перезапуск (див. [opcache\_get\_status()](function.opcache-get-status.md)

### Дивіться також

-   [opcache\_invalidate()](function.opcache-invalidate.md) \- анулює закешований скрипт
-   [opcache\_get\_status()](function.opcache-get-status.md) \- Отримати інформацію про стан кешу
