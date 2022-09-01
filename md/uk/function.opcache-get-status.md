---
navigation:
  - function.opcache-get-configuration.html: « opcachegetconfiguration
  - function.opcache-invalidate.html: opcacheinvalidate »
  - index.html: PHP Manual
  - ref.opcache.html: Функции OPcache
title: opcachegetstatus
---
# opcachegetstatus

(PHP 5> = 5.5.0, PHP 7, PHP 8, PECL ZendOpcache > 7.0.2)

opcachegetstatus — Отримати інформацію про стан кешу

### Опис

```methodsynopsis
opcache_get_status(bool $include_scripts = true): array|false
```

Функція повертає інформацію про стан екземпляра кеша у пам'яті. Вона не повертає жодної інформації про файловий кеш.

### Список параметрів

`include_scripts`

Включити інформацію про стан конкретного сценарію.

### Значення, що повертаються

Повертає масив, що опціонально містить інформацію про стан конкретного скрипту або **`false`** у разі виникнення помилки.

### Помилки

Якщо використовується `opcache.restrict_api` і поточний шлях підпадає під заборону, то буде викликана помилка рівня EWARNING і жодних даних повернуто не буде.

### Дивіться також

-   [opcachegetconfiguration()](function.opcache-get-configuration.html) - Отримати конфігураційну інформацію кешу
