---
navigation:
  - function.sodium-crypto-scalarmult.md: « sodium\_crypto\_scalarmult
  - function.sodium-crypto-secretbox-open.md: sodium\_crypto\_secretbox\_open »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_secretbox\_keygen
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_secretbox\_keygen

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_secretbox\_keygen — Створює випадковий ключ для sodium\_crypto\_secretbox

### Опис

```methodsynopsis
sodium_crypto_secretbox_keygen(): string
```

Створює випадковий ключ для [sodium\_crypto\_secretbox()](function.sodium-crypto-secretbox.md) і [sodium\_crypto\_secretbox\_open()](function.sodium-crypto-secretbox-open.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає згенерований рядок криптографічно безпечних випадкових байтів.

### Приклади

**Пример #1 Пример использования**sodium\_crypto\_secretbox\_keygen()\*\*\*\*

```php
<?php
$key = sodium_crypto_secretbox_keygen();
var_dump( sodium_bin2hex( $key ) );
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(64) "88bd1dc51ec81984f3ddc5a8f59a3d95b647e2da3e879f1b9ceb0abd89e7286c"
```

**Пример #2 Сравнение**sodium\_crypto\_secretbox\_keygen()**с[random\_bytes()](function.random-bytes.md)**

```php
<?php
$key = sodium_crypto_secretbox_keygen();
$bytes = random_bytes( SODIUM_CRYPTO_SECRETBOX_KEYBYTES );
var_dump( mb_strlen( $key, '8bit' ) === mb_strlen( $bytes, '8bit' ) );
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```

### Дивіться також

-   [sodium\_bin2hex()](function.sodium-bin2hex.md) \- Кодувати у шістнадцяткову виставу
-   [random\_bytes()](function.random-bytes.md) \- Отримує криптографічно безпечні випадкові байти
