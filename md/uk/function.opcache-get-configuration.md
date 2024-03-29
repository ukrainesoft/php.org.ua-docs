---
navigation:
  - function.opcache-compile-file.md: « opcache\_compile\_file
  - function.opcache-get-status.md: opcache\_get\_status »
  - index.md: PHP Manual
  - ref.opcache.md: Опції OPcache
title: opcache\_get\_configuration
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# opcache\_get\_configuration

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL ZendOpcache > 7.0.2)

opcache\_get\_configuration — Отримати конфігураційну інформацію кешу

### Опис

```methodsynopsis
opcache_get_configuration(): array|false
```

Ця функція повертає конфігураційні установки екземпляра кеша.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив з інформацією, включаючи INI-налаштування, чорний список та версію

### Помилки

Якщо використовується `opcache.restrict_api` і поточний шлях підпадає під заборону, то буде викликана помилка рівня E\_WARNING і жодних даних повернуто не буде.

### Дивіться також

-   [opcache\_get\_status()](function.opcache-get-status.md) \- Отримати інформацію про стан кешу
