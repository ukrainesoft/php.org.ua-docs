---
navigation:
  - function.opcache-get-configuration.md: « opcache\_get\_configuration
  - function.opcache-invalidate.md: opcache\_invalidate »
  - index.md: PHP Manual
  - ref.opcache.md: Опції OPcache
title: opcache\_get\_status
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# opcache\_get\_status

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL ZendOpcache > 7.0.2)

opcache\_get\_status — Отримати інформацію про стан кешу

### Опис

```methodsynopsis
opcache_get_status(bool $include_scripts = true): array|false
```

Функція повертає інформацію про стан екземпляра кеша у пам'яті. Вона не повертає жодної інформації про файловий кеш.

### Список параметрів

`include_scripts`

Включити інформацію про стан конкретного сценарію.

### Значення, що повертаються

Повертає масив, що опціонально містить інформацію про стан конкретного скрипту або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо використовується `opcache.restrict_api` і поточний шлях підпадає під заборону, то буде викликана помилка рівня E\_WARNING і жодних даних повернуто не буде.

### Дивіться також

-   [opcache\_get\_configuration()](function.opcache-get-configuration.md) \- Отримати конфігураційну інформацію кешу
