---
navigation:
  - function.opcache-invalidate.md: « opcache\_invalidate
  - function.opcache-reset.md: opcache\_reset »
  - index.md: PHP Manual
  - ref.opcache.md: Опції OPcache
title: opcache\_is\_script\_cached
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# opcache\_is\_script\_cached

(PHP 5 >= 5.5.11, PHP 7, PHP 8, PECL ZendOpcache >= 7.0.4)

opcache\_is\_script\_cached — Перевіряє, чи закешовано скрипт в OPCache

### Опис

```methodsynopsis
opcache_is_script_cached(string $filename): bool
```

Функція перевіряє, чи вказаний скрипт закешований в OPCache. Може бути використана для визначення прогріти кеш для конкретного скрипту. Функція перевіряє лише кеш у пам'яті, не перевіряючи файловий кеш.

### Список параметрів

`filename`

Шлях до файлу сценарію.

### Значення, що повертаються

Повертає **`true`**, якщо `filename` закешований в OPCache, **`false`** якщо ні.

### Дивіться також

-   [opcache\_compile\_file()](function.opcache-compile-file.md) \- Скомпілювати та закешувати, але не виконувати скрипт PHP
