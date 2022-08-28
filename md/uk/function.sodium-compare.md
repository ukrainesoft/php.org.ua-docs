Порівняти великі числа

-   [« sodium\_bin2hex](function.sodium-bin2hex.html)
    
-   [sodium\_crypto\_aead\_aes256gcm\_decrypt »](function.sodium-crypto-aead-aes256gcm-decrypt.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Порівняти великі числа
    

# sodiumcompare

(PHP 7> = 7.2.0, PHP 8)

sodiumcompare — Порівняти великі числа

### Опис

```methodsynopsis
sodium_compare(string $string1, string $string2): int
```

Порівнює два рядки, ніби вони були цілими числами довільної довжини без знака з прямим порядком байтів, без витоку з побічного каналу.

### Список параметрів

`string1`

Лівий операнд

`string2`

Правий операнд

### Значення, що повертаються

Повертає `-1`, якщо `string1` менше `string2`

Повертає `1`, якщо `string1` більше `string2`

Повертає `0`якщо рядки рівні.