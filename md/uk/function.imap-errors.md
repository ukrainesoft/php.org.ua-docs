---
navigation:
  - function.imap-deletemailbox.md: « imap\_deletemailbox
  - function.imap-expunge.md: imap\_expunge »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_errors
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_errors

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_errors — Отримує всі помилки, що відбулися IMAP

### Опис

```methodsynopsis
imap_errors(): array|false
```

Повертає всі помилки IMAP (якщо вони є), що відбулися з моменту запиту поточної сторінки або з останнього скидання стека помилок.

Коли викликається функція **imap\_errors()**, стек помилок очищається.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ця функція повертає масив усіх помилок IMAP, що виникли з моменту останнього запуску **imap\_errors()** або від початку сторінки. Якщо таких немає, повертає **`false`**

### Дивіться також

-   [imap\_last\_error()](function.imap-last-error.md) \- Отримує останню помилку IMAP у поточному запиті
-   [imap\_alerts()](function.imap-alerts.md) \- Повертає всі попереджувальні повідомлення IMAP.
