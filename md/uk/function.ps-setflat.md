Встановлює площинність

-   [« ps\_setdash](function.ps-setdash.html)
    
-   [ps\_setfont »](function.ps-setfont.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Встановлює площинність
    

# псsetflat

(PECL ps >= 1.1.0)

псsetflat - Встановлює площинність

### Опис

```methodsynopsis
ps_setflat(resource $psdoc, float $value): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`value`

`value` має бути між 0.2 та 1.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.