Встановлює ширину лінії

-   [«pssetlinejoin](function.ps-setlinejoin.html)
    
-   [псsetmiterlimit »](function.ps-setmiterlimit.html)
    
-   [PHP Manual](index.md)
    
-   [Функції PS](ref.ps.md)
    
-   Встановлює ширину лінії
    

# псsetlinewidth

(PECL ps >= 1.1.0)

псsetlinewidth - Встановлює ширину лінії

### Опис

```methodsynopsis
ps_setlinewidth(resource $psdoc, float $width): bool
```

Встановлює ширину лінії для наступних операцій малювання.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

`width`

Ширина ліній у точках.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псsetlinecap()](function.ps-setlinecap.html) - Встановлює зовнішній вигляд закінчення лінії
-   [псsetlinejoin()](function.ps-setlinejoin.html) - Встановлює спосіб з'єднання ліній
-   [псsetmiterlimit()](function.ps-setmiterlimit.html) - Встановлює межу скосу