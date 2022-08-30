Створює новий об'єкт документа PostScript

-   [«psmoveto](function.ps-moveto.html)
    
-   [псopenfile »](function.ps-open-file.html)
    
-   [PHP Manual](index.md)
    
-   [Функції PS](ref.ps.md)
    
-   Створює новий об'єкт документа PostScript
    

# псnew

(PECL ps >= 1.1.0)

псnew — Створює новий об'єкт документа PostScript

### Опис

```methodsynopsis
ps_new(): resource|false
```

Створює новий екземпляр документа. Функція не створює файл на диску чи пам'яті, вона просто все налаштовує. За **псnew()** зазвичай слідує виклик [псopenfile()](function.ps-open-file.html) для фактичного створення документа postscript.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ресурс документа PostScript або **`false`** у разі виникнення помилки. Значення, що повертається, передається всім іншим функціям як перший аргумент.

### Дивіться також

-   [псdelete()](function.ps-delete.html) - Видаляє всі ресурси документа PostScript