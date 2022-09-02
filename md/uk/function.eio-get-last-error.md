---
navigation:
  - function.eio-get-event-stream.md: « eiogeteventstream
  - function.eio-grp-add.md: eiogrpadd »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eiogetlasterror
---
# eiogetlasterror

(PECL eio >= 1.0.0)

eiogetlasterror — Повертає останню помилку, пов'язану із вказівником на ресурс

### Опис

```methodsynopsis
eio_get_last_error(resource $req): string
```

**eiogetlasterror()** повертає останню помилку, пов'язану із вказівником на ресурс `req`

### Список параметрів

`req`

Покажчик на ресурс

### Значення, що повертаються

**eiogetlasterror()** повертає рядок, що містить останню помилку, пов'язану з вказівником на ресурс `req`

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.
