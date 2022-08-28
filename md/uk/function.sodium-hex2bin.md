Декодує рядок у шістнадцятковому поданні до бінарного

-   [« sodium\_crypto\_stream](function.sodium-crypto-stream.html)
    
-   [sodium\_increment »](function.sodium-increment.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Декодує рядок у шістнадцятковому поданні до бінарного
    

# sodiumhex2bin

(PHP 7> = 7.2.0, PHP 8)

sodiumhex2bin - Декодує рядок у шістнадцятковому поданні в бінарне

### Опис

```methodsynopsis
sodium_hex2bin(string $string, string $ignore = ""): string
```

Декодує рядок, закодований у шістнадцяткове подання до бінарного.

Як і [sodium\_bin2hex()](function.sodium-bin2hex.html), функція **sodiumhex2bin()** стійка до атак по стороннім каналам (side-channel attacks), на відміну функції [hex2bin()](function.hex2bin.html)

### Список параметрів

`string`

Шістнадцяткове представлення даних.

`ignore`

Необов'язковий рядковий аргумент з символами, що ігноруються.

### Значення, що повертаються

Повертає двійкове подання переданих у аргументі `string` даних.