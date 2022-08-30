Застосування бінарного патча до рядка

-   [xdiffstringbdiff](function.xdiff-string-bdiff.html)
    
-   [xdiffstringdiffbinary »](function.xdiff-string-diff-binary.html)
    
-   [PHP Manual](index.md)
    
-   [Функції xdiff](ref.xdiff.md)
    
-   Застосування бінарного патча до рядка
    

# xdiffstringbpatch

(PECL xdiff >= 1.5.0)

xdiffstringbpatch — Застосування бінарного патча до рядка

### Опис

```methodsynopsis
xdiff_string_bpatch(string $str, string $patch): string
```

Застосовує до рядка `str` бінарний патч `patch`. Ця функція приймає патчі створені як [xdiffstringbdiff()](function.xdiff-string-bdiff.html), так і [xdiffstringrabdiff()](function.xdiff-string-rabdiff.html)

### Список параметрів

`str`

Оригінальний бінарний рядок.

`patch`

Рядок з бінарним патчем.

### Значення, що повертаються

Повертає змінений рядок, або **`false`** у разі виникнення помилки.

### Дивіться також

-   [xdiffstringbdiff()](function.xdiff-string-bdiff.html) - Створити бінарний патч для двох рядків
-   [xdiffstringrabdiff()](function.xdiff-string-rabdiff.html) - Порівняти два рядки та створити бінарний патч використовуючи поліномінальний алгоритм Rabin fingerprint