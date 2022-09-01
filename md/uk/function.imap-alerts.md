---
navigation:
  - function.imap-8bit.html: « imap8bit
  - function.imap-append.html: imapappend »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapalerts
---
# imapalerts

(PHP 4, PHP 5, PHP 7, PHP 8)

imapalerts — Повертає всі попереджувальні повідомлення IMAP.

### Опис

```methodsynopsis
imap_alerts(): array|false
```

Повертає всі створені попереджувальні повідомлення IMAP з моменту останнього дзвінка **imapalerts()**, або під час завантаження сторінки.

Коли **imapalerts()** викликається, стек попереджень очищається. Специфікація IMAP вимагає, щоб ці повідомлення були надіслані користувачеві.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив усіх створених попереджувальних повідомлень IMAP або **`false`** якщо таких немає.

### Дивіться також

-   [imaperrors()](function.imap-errors.html) - Отримати всі помилки, що відбулися IMAP
