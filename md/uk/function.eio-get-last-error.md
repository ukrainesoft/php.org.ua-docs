---
navigation:
  - function.eio-get-event-stream.md: « eio\_get\_event\_stream
  - function.eio-grp-add.md: eio\_grp\_add »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_get\_last\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_get\_last\_error

(PECL eio >= 1.0.0)

eio\_get\_last\_error — Повертає останню помилку, пов'язану із вказівником на ресурс

### Опис

```methodsynopsis
eio_get_last_error(resource $req): string
```

**eio\_get\_last\_error()** повертає останню помилку, пов'язану із вказівником на ресурс `req`

### Список параметрів

`req`

Покажчик на ресурс

### Значення, що повертаються

**eio\_get\_last\_error()** повертає рядок, що містить останню помилку, пов'язану з вказівником на ресурс `req`

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.
