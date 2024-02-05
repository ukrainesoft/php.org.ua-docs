---
navigation:
  - function.xdiff-string-bdiff-size.md: « xdiff\_string\_bdiff\_size
  - function.xdiff-string-bpatch.md: xdiff\_string\_bpatch »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdiff\_string\_bdiff
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xdiff\_string\_bdiff

(PECL xdiff >= 1.5.0)

xdiff\_string\_bdiff — Створити бінарний патч для двох рядків

### Опис

```methodsynopsis
xdiff_string_bdiff(string $old_data, string $new_data): string
```

Здійснює бінарне порівняння двох рядків та повертає патч. Ця функція працює як з текстом, так і з бінарними даними. Отриманий патч згодом можна застосувати за допомогою функцій [xdiff\_string\_bpatch()](function.xdiff-string-bpatch.md) і [xdiff\_file\_bpatch()](function.xdiff-file-bpatch.md)

### Список параметрів

`old_data`

Перший рядок із бінарними даними. Це будуть "старі" дані.

`new_data`

Другий рядок із бінарними даними. Це будуть "нові" дані.

### Значення, що повертаються

Повертає рядок з бінарним патчем, що містить різницю між "старими" та "новими" даними, або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [xdiff\_string\_bpatch()](function.xdiff-string-bpatch.md) \- Застосування бінарного патча до рядка
