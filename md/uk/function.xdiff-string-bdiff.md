---
navigation:
  - function.xdiff-string-bdiff-size.html: xdiffstringbdiffsize
  - function.xdiff-string-bpatch.html: xdiffstringbpatch »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdiffstringbdiff
---
# xdiffstringbdiff

(PECL xdiff >= 1.5.0)

xdiffstringbdiff — Створити бінарний патч для двох рядків

### Опис

```methodsynopsis
xdiff_string_bdiff(string $old_data, string $new_data): string
```

Здійснює бінарне порівняння двох рядків та повертає патч. Ця функція працює як з текстом, так і з бінарними даними. Отриманий патч згодом можна застосувати за допомогою функцій [xdiffstringbpatch()](function.xdiff-string-bpatch.html) і [xdifffilebpatch()](function.xdiff-file-bpatch.html)

### Список параметрів

`old_data`

Перший рядок із бінарними даними. Це будуть "старі" дані.

`new_data`

Другий рядок із бінарними даними. Це будуть "нові" дані.

### Значення, що повертаються

Повертає рядок з бінарним патчем, що містить різницю між "старими" та "новими" даними, або **`false`** у разі виникнення помилки.

### Дивіться також

-   [xdiffstringbpatch()](function.xdiff-string-bpatch.html) - Застосування бінарного патча до рядка
