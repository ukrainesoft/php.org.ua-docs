Встановлює спосіб з'єднання ліній

-   [«pssetlinecap](function.ps-setlinecap.html)
    
-   [псsetlinewidth »](function.ps-setlinewidth.html)
    
-   [PHP Manual](index.md)
    
-   [Функції PS](ref.ps.md)
    
-   Встановлює спосіб з'єднання ліній
    

# псsetlinejoin

(PECL ps >= 1.1.0)

псsetlinejoin - Встановлює спосіб з'єднання ліній

### Опис

```methodsynopsis
ps_setlinejoin(resource $psdoc, int $type): bool
```

Встановлює спосіб з'єднання ліній.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

`type`

Спосіб з'єднання ліній. Можливі значення: `PS_LINEJOIN_MITER` `PS_LINEJOIN_ROUND` або `PS_LINEJOIN_BEVEL`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псsetlinecap()](function.ps-setlinecap.html) - Встановлює зовнішній вигляд закінчення лінії
-   [псsetlinewidth()](function.ps-setlinewidth.html) - Встановлює ширину лінії
-   [псsetmiterlimit()](function.ps-setmiterlimit.html) - Встановлює межу скосу