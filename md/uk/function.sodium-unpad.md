Видалення даних відступів

-   [« sodiumpad](function.sodium-pad.html)
    
-   [SodiumException »](class.sodiumexception.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Видалення даних відступів
    

# sodiumunpad

(PHP 7> = 7.2.0, PHP 8)

sodiumunpad — Видалення даних відступів

### Опис

```methodsynopsis
sodium_unpad(string $string, int $block_size): string
```

Видаляє дані відступів у доповненого рядка. Безпечна за часом.

### Список параметрів

`string`

Доповнений рядок.

`block_size`

Розмір блоку заповнення.

### Значення, що повертаються

Стоку з віддаленими відступами.