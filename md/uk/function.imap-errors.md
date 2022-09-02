---
navigation:
  - function.imap-deletemailbox.md: « imapdeletemailbox
  - function.imap-expunge.md: imapexpunge »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imaperrors
---
# imaperrors

(PHP 4, PHP 5, PHP 7, PHP 8)

imaperrors — Отримати всі помилки, що відбулися IMAP

### Опис

```methodsynopsis
imap_errors(): array|false
```

Повертає всі помилки IMAP (якщо вони є), що відбулися з моменту запиту поточної сторінки або з останнього скидання стека помилок.

Коли викликається функція **imaperrors()**, стек помилок очищається.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ця функція повертає масив усіх помилок IMAP, що виникли з моменту останнього запуску **imaperrors()** або від початку сторінки. Якщо таких немає, повертає **`false`**

### Дивіться також

-   [imaplasterror()](function.imap-last-error.md) - Отримати останню помилку IMAP у поточному запиті
-   [imapalerts()](function.imap-alerts.md) - Повертає всі попереджувальні повідомлення IMAP.
