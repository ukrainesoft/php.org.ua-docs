Встановлює зовнішній вигляд закінчення лінії

-   [«pssetgray](function.ps-setgray.html)
    
-   [псsetlinejoin »](function.ps-setlinejoin.html)
    
-   [PHP Manual](index.md)
    
-   [Функції PS](ref.ps.md)
    
-   Встановлює зовнішній вигляд закінчення лінії
    

# псsetlinecap

(PECL ps >= 1.1.0)

псsetlinecap - Встановлює зовнішній вигляд закінчення лінії

### Опис

```methodsynopsis
ps_setlinecap(resource $psdoc, int $type): bool
```

Встановлює зовнішній вигляд закінчення лінії.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

`type`

Тип закінчення лінії. Можливі значення: `PS_LINECAP_BUTT` `PS_LINECAP_ROUND` або `PS_LINECAP_SQUARED`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псsetlinejoin()](function.ps-setlinejoin.html) - Встановлює спосіб з'єднання ліній
-   [псsetlinewidth()](function.ps-setlinewidth.html) - Встановлює ширину лінії
-   [псsetmiterlimit()](function.ps-setmiterlimit.html) - Встановлює межу скосу