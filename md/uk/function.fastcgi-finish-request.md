---
navigation:
  - ref.fpm.md: « Функції FPM
  - function.fpm-get-status.md: fpm\_get\_status »
  - index.md: PHP Manual
  - ref.fpm.md: Функції FPM
title: fastcgi\_finish\_request
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fastcgi\_finish\_request

(PHP 5 >= 5.3.3, PHP 7, PHP 8)

fastcgi\_finish\_request — Скидає всі дані клієнту.

### Опис

```methodsynopsis
fastcgi_finish_request(): bool
```

Ця функція скидає всі запитані дані клієнта та завершує обробку запиту. Це дозволяє виконувати тривалі завдання без підтримки зв'язку з клієнтом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
