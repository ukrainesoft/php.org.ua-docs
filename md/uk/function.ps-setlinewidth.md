Встановлює ширину лінії

-   [« ps\_setlinejoin](function.ps-setlinejoin.html)
    
-   [ps\_setmiterlimit »](function.ps-setmiterlimit.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
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

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`width`

Ширина ліній у точках.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_setlinecap()](function.ps-setlinecap.html) - Встановлює зовнішній вигляд закінчення лінії
-   [ps\_setlinejoin()](function.ps-setlinejoin.html) - Встановлює спосіб з'єднання ліній
-   [ps\_setmiterlimit()](function.ps-setmiterlimit.html) - Встановлює межу скосу