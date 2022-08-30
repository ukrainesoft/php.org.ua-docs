Створює випадковий ключ для sodiumcryptosecretbox

-   [« sodiumcryptoscalarmult](function.sodium-crypto-scalarmult.html)
    
-   [sodiumcryptosecretboxopen »](function.sodium-crypto-secretbox-open.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Sodium](ref.sodium.md)
    
-   Створює випадковий ключ для sodiumcryptosecretbox
    

# sodiumcryptosecretboxkeygen

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosecretboxkeygen — Створює випадковий ключ для sodiumcryptosecretbox

### Опис

```methodsynopsis
sodium_crypto_secretbox_keygen(): string
```

Створює випадковий ключ для [sodiumcryptosecretbox()](function.sodium-crypto-secretbox.html) і [sodiumcryptosecretboxopen()](function.sodium-crypto-secretbox-open.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає згенерований рядок криптографічно безпечних випадкових байтів.

### Приклади

**Приклад #1 Приклад використання **sodiumcryptosecretboxkeygen()****

```php
<?php
$key = sodium_crypto_secretbox_keygen();
var_dump( sodium_bin2hex( $key ) );
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(64) "88bd1dc51ec81984f3ddc5a8f59a3d95b647e2da3e879f1b9ceb0abd89e7286c"
```

**Приклад #2 Порівняння **sodiumcryptosecretboxkeygen()** з [randombytes()](function.random-bytes.html)**

```php
<?php
$key = sodium_crypto_secretbox_keygen();
$bytes = random_bytes( SODIUM_CRYPTO_SECRETBOX_KEYBYTES );
var_dump( mb_strlen( $key, '8bit' ) === mb_strlen( $bytes, '8bit' ) );
?>
```

Результат виконання цього прикладу:

```
bool(true)
```

### Дивіться також

-   [sodiumbin2hex()](function.sodium-bin2hex.html) - Кодувати у шістнадцяткову виставу
-   [randombytes()](function.random-bytes.html) - Генерує криптографічно безпечні псевдовипадкові байти