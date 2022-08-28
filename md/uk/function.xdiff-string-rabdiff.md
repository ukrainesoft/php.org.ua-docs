Порівняти два рядки та створити бінарний патч використовуючи поліномінальний алгоритм Rabin fingerprint

-   [« xdiff\_string\_patch](function.xdiff-string-patch.html)
    
-   [Поддержка языков и кодировок »](refs.international.html)
    
-   [PHP Manual](index.html)
    
-   [Функции xdiff](ref.xdiff.html)
    
-   Порівняти два рядки та створити бінарний патч використовуючи поліномінальний алгоритм Rabin fingerprint
    

# xdiffstringrabdiff

(PECL xdiff >= 1.5.0)

xdiffstringrab diff — Порівняти два рядки і створити бінарний патч, використовуючи поліноміальний алгоритм Rabin fingerprint

### Опис

```methodsynopsis
xdiff_string_bdiff(string $old_data, string $new_data): string
```

Створює бінарний патч для двох рядків та повертає результат. Різниця між цією функцією та [xdiff\_string\_bdiff()](function.xdiff-string-bdiff.html) у алгоритмі, який працює швидше і створює більш короткий патч. Ця функція працює як із текстовими, так і з бінарними даними. Отриманий патч згодом можна застосувати за допомогою функцій [xdiff\_string\_bpatch()](function.xdiff-string-bpatch.html) і [xdiff\_file\_bpatch()](function.xdiff-file-bpatch.html)

Детальніше про відмінності в алгоритмах читайте на сайті [» libxdiff](http://www.xmailserver.org/xdiff-lib.html)

### Список параметрів

`old_data`

Перший рядок із бінарними даними. Це будуть "старі" дані.

`new_data`

Другий рядок із бінарними даними. Це будуть "нові" дані.

### Значення, що повертаються

Повертає рядок з бінарним патчем, що містить різницю між "старими" та "новими" даними, або **`false`** у разі виникнення помилки.

### Дивіться також

-   [xdiff\_string\_bpatch()](function.xdiff-string-bpatch.html) - Застосування бінарного патча до рядка