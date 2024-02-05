---
navigation:
  - function.xdiff-string-patch.md: « xdiff\_string\_patch
  - refs.international.md: Підтримка мов та кодувань »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdiff\_string\_rabdiff
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xdiff\_string\_rabdiff

(PECL xdiff >= 1.5.0)

xdiff\_string\_rab diff — Порівняти два рядки і створити бінарний патч, використовуючи поліноміальний алгоритм Rabin fingerprint

### Опис

```methodsynopsis
xdiff_string_bdiff(string $old_data, string $new_data): string
```

Створює бінарний патч для двох рядків та повертає результат. Різниця між цією функцією та [xdiff\_string\_bdiff()](function.xdiff-string-bdiff.md) у алгоритмі, який працює швидше і створює більш короткий патч. Ця функція працює як із текстовими, так і з бінарними даними. Отриманий патч згодом можна застосувати за допомогою функцій [xdiff\_string\_bpatch()](function.xdiff-string-bpatch.md) і [xdiff\_file\_bpatch()](function.xdiff-file-bpatch.md)

Более подробно о различиях в алгоритмах читайте на сайте[» libxdiff](http://www.xmailserver.org/xdiff-lib.md)

### Список параметрів

`old_data`

Перший рядок із бінарними даними. Це будуть "старі" дані.

`new_data`

Другий рядок із бінарними даними. Це будуть "нові" дані.

### Значення, що повертаються

Повертає рядок з бінарним патчем, що містить різницю між "старими" та "новими" даними, або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [xdiff\_string\_bpatch()](function.xdiff-string-bpatch.md) \- Застосування бінарного патча до рядка
