Доповнює рядок відступами

-   [« sodiummemzero](function.sodium-memzero.html)
    
-   [sodiumunpad »](function.sodium-unpad.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Sodium](ref.sodium.md)
    
-   Доповнює рядок відступами
    

# sodiumpad

(PHP 7> = 7.2.0, PHP 8)

sodiumpad — Доповнює рядок відступами

### Опис

```methodsynopsis
sodium_pad(string $string, int $block_size): string
```

Доповнює рядок праворуч до заданої довжини. Безпечна за часом.

### Список параметрів

`string`

Вхідний рядок.

`block_size`

Рядок буде доповнено доти, доки вона не стане парною кратною розміру блоку.

### Значення, що повертаються

Доповнений рядок.