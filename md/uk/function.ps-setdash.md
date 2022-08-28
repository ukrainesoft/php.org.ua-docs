Встановлює зовнішній вигляд пунктирної лінії

-   [« ps\_setcolor](function.ps-setcolor.html)
    
-   [ps\_setflat »](function.ps-setflat.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Встановлює зовнішній вигляд пунктирної лінії
    

# псsetdash

(PECL ps >= 1.1.0)

псsetdash - Встановлює зовнішній вигляд пунктирної лінії

### Опис

```methodsynopsis
ps_setdash(resource $psdoc, float $on, float $off): bool
```

Встановлює довжину чорних та білих частин пунктирної лінії.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`on`

Довжина рисочки.

`off`

Довжина проміжку між рисочками.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_setpolydash()](function.ps-setpolydash.html) - Встановлює зовнішній вигляд пунктирної лінії