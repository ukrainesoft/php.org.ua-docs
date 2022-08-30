Псевдонім для xdiffstringbpatch

-   [xdiffstringmerge3](function.xdiff-string-merge3.html)
    
-   [xdiffstringpatch »](function.xdiff-string-patch.html)
    
-   [PHP Manual](index.md)
    
-   [Функції xdiff](ref.xdiff.md)
    
-   Псевдонім для xdiffstringbpatch
    

# xdiffstringpatchbinary

(PECL xdiff >= 0.2.0)

xdiffstringpatchbinary - Псевдонім для xdiffstringbpatch

### Опис

```methodsynopsis
xdiff_string_patch_binary(string $str, string $patch): string
```

Застосовує до рядка `str` бінарний патч `patch`. Ця функція приймає патчі створені як [xdiffstringbdiff()](function.xdiff-string-bdiff.html), так і [xdiffstringrabdiff()](function.xdiff-string-rabdiff.html)

Починаючи з версії 1.5.0 є псевдонімом для [xdiffstringbpatch()](function.xdiff-string-bpatch.html)

### Список параметрів

`str`

Оригінальний бінарний рядок.

`patch`

Рядок з бінарним патчем.

### Значення, що повертаються

Повертає змінений рядок, або **`false`** у разі виникнення помилки.

### Дивіться також

-   [xdiffstringbpatch()](function.xdiff-string-bpatch.html) - Застосування бінарного патча до рядка
-   [xdiffstringbdiff()](function.xdiff-string-bdiff.html) - Створити бінарний патч для двох рядків
-   [xdiffstringrabdiff()](function.xdiff-string-rabdiff.html) - Порівняти два рядки та створити бінарний патч використовуючи поліномінальний алгоритм Rabin fingerprint