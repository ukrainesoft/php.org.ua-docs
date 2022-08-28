Встановлює спосіб з'єднання ліній

-   [« ps\_setlinecap](function.ps-setlinecap.html)
    
-   [ps\_setlinewidth »](function.ps-setlinewidth.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
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

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`type`

Спосіб з'єднання ліній. Можливі значення: `PS_LINEJOIN_MITER` `PS_LINEJOIN_ROUND` або `PS_LINEJOIN_BEVEL`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_setlinecap()](function.ps-setlinecap.html) - Встановлює зовнішній вигляд закінчення лінії
-   [ps\_setlinewidth()](function.ps-setlinewidth.html) - Встановлює ширину лінії
-   [ps\_setmiterlimit()](function.ps-setmiterlimit.html) - Встановлює межу скосу