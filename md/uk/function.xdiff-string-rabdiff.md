---
navigation:
  - function.xdiff-string-patch.html: xdiffstringpatch
  - refs.international.md: Підтримка мов та кодувань »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdiffstringrabdiff
---
# xdiffstringrabdiff

(PECL xdiff >= 1.5.0)

xdiffstringrab diff — Порівняти два рядки і створити бінарний патч, використовуючи поліноміальний алгоритм Rabin fingerprint

### Опис

```methodsynopsis
xdiff_string_bdiff(string $old_data, string $new_data): string
```

Створює бінарний патч для двох рядків та повертає результат. Різниця між цією функцією та [xdiffstringbdiff()](function.xdiff-string-bdiff.html) у алгоритмі, який працює швидше і створює більш короткий патч. Ця функція працює як із текстовими, так і з бінарними даними. Отриманий патч згодом можна застосувати за допомогою функцій [xdiffstringbpatch()](function.xdiff-string-bpatch.html) і [xdifffilebpatch()](function.xdiff-file-bpatch.md)

Детальніше про відмінності в алгоритмах читайте на сайті [» libxdiff](http://www.xmailserver.org/xdiff-lib.md)

### Список параметрів

`old_data`

Перший рядок із бінарними даними. Це будуть "старі" дані.

`new_data`

Другий рядок із бінарними даними. Це будуть "нові" дані.

### Значення, що повертаються

Повертає рядок з бінарним патчем, що містить різницю між "старими" та "новими" даними, або **`false`** у разі виникнення помилки.

### Дивіться також

-   [xdiffstringbpatch()](function.xdiff-string-bpatch.md) - Застосування бінарного патча до рядка
