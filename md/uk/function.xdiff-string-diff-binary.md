---
navigation:
  - function.xdiff-string-bpatch.html: xdiffstringbpatch
  - function.xdiff-string-diff.html: xdiffstringdiff »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdiffstringdiffbinary
---
# xdiffstringdiffbinary

(PECL xdiff >= 0.2.0)

xdiffstringdiffbinary - Псевдонім для xdiffstringbdiff

### Опис

```methodsynopsis
xdiff_string_bdiff(string $old_data, string $new_data): string
```

Здійснює бінарне порівняння двох рядків та повертає патч. Ця функція працює як з текстом, так і з бінарними даними. Отриманий патч згодом можна застосувати за допомогою функцій [xdiffstringbpatch()](function.xdiff-string-bpatch.html) і [xdifffilebpatch()](function.xdiff-file-bpatch.html)

Починаючи з версії 1.5.0 є псевдонімом для [xdiffstringbdiff()](function.xdiff-string-bdiff.html)

### Список параметрів

`old_data`

Перший рядок із бінарними даними. Це будуть "старі" дані.

`new_data`

Другий рядок із бінарними даними. Це будуть "нові" дані.

### Значення, що повертаються

Повертає рядок з бінарним патчем, що містить різницю між "старими" та "новими" даними, або **`false`** у разі виникнення помилки.

### Дивіться також

-   [xdiffstringbdiff()](function.xdiff-string-bdiff.html) - Створити бінарний патч для двох рядків
-   [xdiffstringbpatch()](function.xdiff-string-bpatch.html) - Застосування бінарного патча до рядка
