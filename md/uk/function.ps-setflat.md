Встановлює площинність

-   [«pssetdash](function.ps-setdash.html)
    
-   [псsetfont »](function.ps-setfont.html)
    
-   [PHP Manual](index.md)
    
-   [Функції PS](ref.ps.md)
    
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

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

`value`

`value` має бути між 0.2 та 1.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.