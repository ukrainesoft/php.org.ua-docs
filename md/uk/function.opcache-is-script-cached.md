---
navigation:
  - function.opcache-invalidate.md: « opcacheinvalidate
  - function.opcache-reset.md: opcachereset »
  - index.md: PHP Manual
  - ref.opcache.md: Функции OPcache
title: opcacheісscriptcached
---
# opcacheісscriptcached

(PHP 5> = 5.5.11, PHP 7, PHP 8, PECL ZendOpcache> = 7.0.4)

opcacheісscriptcached — Перевіряє, чи закешовано скрипт в OPCache

### Опис

```methodsynopsis
opcache_is_script_cached(string $filename): bool
```

Функція перевіряє, чи вказаний скрипт в OPCache. Може бути використана для визначення прогріти кеш для конкретного скрипту. Функція перевіряє лише кеш у пам'яті, не перевіряючи файловий кеш.

### Список параметрів

`filename`

Шлях до файлу сценарію.

### Значення, що повертаються

Повертає **`true`**, якщо `filename` закешований в OPCache, **`false`** якщо ні.

### Дивіться також

-   [opcachecompilefile()](function.opcache-compile-file.md) - Скомпілювати та закешувати, але не виконувати скрипт PHP
