---
navigation:
  - function.imap-is-open.md: « imap\_is\_open
  - function.imap-list.md: imap\_list »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_last\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_last\_error

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_last\_error — Отримує останню помилку IMAP у поточному запиті

### Опис

```methodsynopsis
imap_last_error(): string|false
```

Повертає повний текст помилки IMAP на поточній сторінці. Стек помилок не торкнеться; наступний виклик \*\*imap\_last\_error()\*\*якщо помилок більше не було, поверне ту ж саму помилку.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає повний текст помилки IMAP на поточній сторінці. Якщо помилок не було – поверне **`false`**

### Дивіться також

-   [imap\_errors()](function.imap-errors.md) \- Отримує всі помилки, що відбулися IMAP
