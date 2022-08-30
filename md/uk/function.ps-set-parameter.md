Встановлює певні параметри

-   [«pssetinfo](function.ps-set-info.html)
    
-   [псsettextpos »](function.ps-set-text-pos.html)
    
-   [PHP Manual](index.html)
    
-   [Функції PS](ref.ps.html)
    
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

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

`name`

Список можливих імен дивіться [псgetparameter()](function.ps-get-parameter.html)

`value`

Значення параметру.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   **псgetparameters()**
-   [псsetvalue()](function.ps-set-value.html) - Встановлює певні значення