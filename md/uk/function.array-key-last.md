Отримує останній ключ масиву

-   [« arraykeyfirst](function.array-key-first.html)
    
-   [arraykeys »](function.array-keys.html)
    
-   [PHP Manual](index.md)
    
-   [Функції для роботи з масивами](ref.array.md)
    
-   Отримує останній ключ масиву
    

# arraykeylast

(PHP 7> = 7.3.0, PHP 8)

arraykeylast — Отримує останній ключ масиву

### Опис

```methodsynopsis
array_key_last(array $array): int|string|null
```

Отримати останній ключ заданого масиву `array`, не торкаючись внутрішнього покажчика масиву.

### Список параметрів

`array`

Масив.

### Значення, що повертаються

Повертає останній ключ масиву `array`якщо він не порожній; **`null`** в іншому випадку.

### Дивіться також

-   [arraykeyfirst()](function.array-key-first.html) - Отримує перший ключ масиву
-   [end()](function.end.md) - Встановлює внутрішній покажчик масиву на його останній елемент