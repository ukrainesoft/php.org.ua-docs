Встановлює певні параметри

-   [« ps\_set\_info](function.ps-set-info.html)
    
-   [ps\_set\_text\_pos »](function.ps-set-text-pos.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Встановлює певні параметри
    

# псsetparameter

(PECL ps >= 1.1.0)

псsetparameter — Встановлює певні параметри

### Опис

```methodsynopsis
ps_set_parameter(resource $psdoc, string $name, string $value): bool
```

Встановлює кілька параметрів, які використовують багато функцій. Параметри визначення є строковими значеннями.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`name`

Список можливих імен дивіться [ps\_get\_parameter()](function.ps-get-parameter.html)

`value`

Значення параметру.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   **псgetparameters()**
-   [ps\_set\_value()](function.ps-set-value.html) - Встановлює певні значення