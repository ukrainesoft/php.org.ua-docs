---
navigation:
  - function.imap-8bit.md: « imap\_8bit
  - function.imap-append.md: imap\_append »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_alerts
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_alerts

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_alerts — Повертає всі попереджувальні повідомлення IMAP.

### Опис

```methodsynopsis
imap_alerts(): array|false
```

Повертає всі створені попереджувальні повідомлення IMAP з моменту останнього дзвінка **imap\_alerts()**, або під час завантаження сторінки.

Когда**imap\_alerts()** викликається, стек попереджень очищається. Специфікація IMAP вимагає, щоб ці повідомлення були надіслані користувачеві.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив усіх створених попереджувальних повідомлень IMAP або **`false`** якщо таких немає.

### Дивіться також

-   [imap\_errors()](function.imap-errors.md) \- Отримує всі помилки, що відбулися IMAP
