---
navigation:
  - ref.fpm.md: « Функції FPM
  - function.fpm-get-status.md: fpmgetstatus »
  - index.md: PHP Manual
  - ref.fpm.md: Функції FPM
title: fastcgifinishrequest
---
# fastcgifinishrequest

(PHP 5> = 5.3.3, PHP 7, PHP 8)

fastcgifinishrequest — Скидає всі дані клієнту.

### Опис

```methodsynopsis
fastcgi_finish_request(): bool
```

Ця функція скидає всі запитані дані клієнта та завершує обробку запиту. Це дозволяє виконувати тривалі завдання без підтримки зв'язку з клієнтом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
