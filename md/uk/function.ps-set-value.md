Встановлює певні значення

-   [«pssettextpos](function.ps-set-text-pos.html)
    
-   [псsetcolor »](function.ps-setcolor.html)
    
-   [PHP Manual](index.md)
    
-   [Функції PS](ref.ps.md)
    
-   Встановлює певні значення
    

# псsetvalue

(PECL ps >= 1.1.0)

псsetvalue — Встановлює певні значення

### Опис

```methodsynopsis
ps_set_value(resource $psdoc, string $name, float $value): bool
```

Встановлює декілька значень, що використовуються багатьма функціями. Параметри визначення є значеннями з плаваючою точкою.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

`name`

Значення `name` може бути одне з наступного:

textrendering

Спосіб відображення тексту.

textx

Координата X для виведення тексту.

texty

Координата Y для виведення тексту.

wordspacing

Відстань між словами щодо ширини пробілу.

leading

Відстань між рядками у пікселях.

`value`

Значення параметру.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псgetvalue()](function.ps-get-value.html) - Отримує певні значення
-   [псsetparameter()](function.ps-set-parameter.html) - Встановлює певні параметри