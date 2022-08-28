Псевдонім для xdiffstringbdiff

-   [« xdiff\_string\_bpatch](function.xdiff-string-bpatch.html)
    
-   [xdiff\_string\_diff »](function.xdiff-string-diff.html)
    
-   [PHP Manual](index.html)
    
-   [Функции xdiff](ref.xdiff.html)
    
-   Псевдонім для xdiffstringbdiff
    

# xdiffstringdiffbinary

(PECL xdiff >= 0.2.0)

xdiffstringdiffbinary - Псевдонім для xdiffstringbdiff

### Опис

```methodsynopsis
xdiff_string_bdiff(string $old_data, string $new_data): string
```

Здійснює бінарне порівняння двох рядків та повертає патч. Ця функція працює як з текстом, так і з бінарними даними. Отриманий патч згодом можна застосувати за допомогою функцій [xdiff\_string\_bpatch()](function.xdiff-string-bpatch.html) і [xdiff\_file\_bpatch()](function.xdiff-file-bpatch.html)

Починаючи з версії 1.5.0 є псевдонімом для [xdiff\_string\_bdiff()](function.xdiff-string-bdiff.html)

### Список параметрів

`old_data`

Перший рядок із бінарними даними. Це будуть "старі" дані.

`new_data`

Другий рядок із бінарними даними. Це будуть "нові" дані.

### Значення, що повертаються

Повертає рядок з бінарним патчем, що містить різницю між "старими" та "новими" даними, або **`false`** у разі виникнення помилки.

### Дивіться також

-   [xdiff\_string\_bdiff()](function.xdiff-string-bdiff.html) - Створити бінарний патч для двох рядків
-   [xdiff\_string\_bpatch()](function.xdiff-string-bpatch.html) - Застосування бінарного патча до рядка