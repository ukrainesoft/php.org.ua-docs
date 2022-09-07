---
navigation:
  - function.opcache-compile-file.md: « opcachecompilefile
  - function.opcache-get-status.md: opcachegetstatus »
  - index.md: PHP Manual
  - ref.opcache.md: Функции OPcache
title: opcachegetconfiguration
---
# opcachegetconfiguration

(PHP 5> = 5.5.0, PHP 7, PHP 8, PECL ZendOpcache > 7.0.2)

opcachegetconfiguration — Отримати конфігураційну інформацію кешу

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

Якщо використовується `opcache.restrict_api` і поточний шлях підпадає під заборону, то буде викликана помилка рівня EWARNING і жодних даних повернуто не буде.

### Дивіться також

-   [opcachegetstatus()](function.opcache-get-status.md) - Отримати інформацію про стан кешу
