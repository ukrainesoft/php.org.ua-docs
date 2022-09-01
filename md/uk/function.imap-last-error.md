---
navigation:
  - function.imap-headers.html: « imapheaders
  - function.imap-list.html: imaplist »
  - index.html: PHP Manual
  - ref.imap.html: Функции IMAP
title: imaplasterror
---
# imaplasterror

(PHP 4, PHP 5, PHP 7, PHP 8)

imaplasterror — Отримати останню помилку IMAP у поточному запиті

### Опис

```methodsynopsis
imap_last_error(): string|false
```

Повертає повний текст помилки IMAP на поточній сторінці. Стек помилок не торкнеться; наступний виклик \*\*imaplasterror()\*\*якщо помилок більше не було, поверне ту ж саму помилку.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає повний текст помилки IMAP на поточній сторінці. Якщо помилок не було – поверне **`false`**

### Дивіться також

-   [imaperrors()](function.imap-errors.html) - Отримати всі помилки, що відбулися IMAP
