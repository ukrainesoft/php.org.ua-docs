Встановлює зовнішній вигляд пунктирної лінії

-   [«pssetcolor](function.ps-setcolor.html)
    
-   [псsetflat »](function.ps-setflat.html)
    
-   [PHP Manual](index.html)
    
-   [Функції PS](ref.ps.html)
    
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

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

`on`

Довжина рисочки.

`off`

Довжина проміжку між рисочками.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псsetpolydash()](function.ps-setpolydash.html) - Встановлює зовнішній вигляд пунктирної лінії