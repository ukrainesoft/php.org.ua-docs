Отримує останній ключ масиву

-   [« array\_key\_first](function.array-key-first.html)
    
-   [array\_keys »](function.array-keys.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с массивами](ref.array.html)
    
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

-   [array\_key\_first()](function.array-key-first.html) - Отримує перший ключ масиву
-   [end()](function.end.html) - Встановлює внутрішній покажчик масиву на його останній елемент