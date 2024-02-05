---
navigation:
  - migration81.new-classes.md: « Нові класи та інтерфейси
  - migration81.constants.md: Нові глобальні константи »
  - index.md: PHP Manual
  - migration81.md: Міграція з PHP 8.0.x на PHP 8.1.x
title: Нові функції
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Нові функції

### Ядро PHP

-   [array\_is\_list()](function.array-is-list.md)

### GD

-   [imagecreatefromavif()](function.imagecreatefromavif.md)
-   [imageavif()](function.imageavif.md)

### MySQLi

-   [mysqli\_result::fetch\_column()](mysqli-result.fetch-column.md)
-   [mysqli\_fetch\_column()](mysqli-result.fetch-column.md)

### Управління процесами

-   [pcntl\_rfork()](function.pcntl-rfork.md)

### Reflection

-   [ReflectionFunctionAbstract::getClosureUsedVariables()](reflectionfunctionabstract.getclosureusedvariables.md)

### Стандартні функції

-   [fsync()](function.fsync.md)
-   [fdatasync()](function.fdatasync.md)

### Sodium

#### XChaCha20

-   [sodium\_crypto\_stream\_xchacha20()](function.sodium-crypto-stream-xchacha20.md)
-   [sodium\_crypto\_stream\_xchacha20\_keygen()](function.sodium-crypto-stream-xchacha20-keygen.md)
-   [sodium\_crypto\_stream\_xchacha20\_xor()](function.sodium-crypto-stream-xchacha20-xor.md)

#### Ristretto255

Функції Ristretto255 доступні з libsodium 1.0.18.

-   [sodium\_crypto\_core\_ristretto255\_add()](function.sodium-crypto-core-ristretto255-add.md)
-   [sodium\_crypto\_core\_ristretto255\_from\_hash()](function.sodium-crypto-core-ristretto255-from-hash.md)
-   [sodium\_crypto\_core\_ristretto255\_is\_valid\_point()](function.sodium-crypto-core-ristretto255-is-valid-point.md)
-   [sodium\_crypto\_core\_ristretto255\_random()](function.sodium-crypto-core-ristretto255-random.md)
-   [sodium\_crypto\_core\_ristretto255\_scalar\_add()](function.sodium-crypto-core-ristretto255-scalar-add.md)
-   [sodium\_crypto\_core\_ristretto255\_scalar\_complement()](function.sodium-crypto-core-ristretto255-scalar-complement.md)
-   [sodium\_crypto\_core\_ristretto255\_scalar\_invert()](function.sodium-crypto-core-ristretto255-scalar-invert.md)
-   [sodium\_crypto\_core\_ristretto255\_scalar\_mul()](function.sodium-crypto-core-ristretto255-scalar-mul.md)
-   [sodium\_crypto\_core\_ristretto255\_scalar\_negate()](function.sodium-crypto-core-ristretto255-scalar-negate.md)
-   [sodium\_crypto\_core\_ristretto255\_scalar\_random()](function.sodium-crypto-core-ristretto255-scalar-random.md)
-   [sodium\_crypto\_core\_ristretto255\_scalar\_reduce()](function.sodium-crypto-core-ristretto255-scalar-reduce.md)
-   [sodium\_crypto\_core\_ristretto255\_scalar\_sub()](function.sodium-crypto-core-ristretto255-scalar-sub.md)
-   [sodium\_crypto\_core\_ristretto255\_sub()](function.sodium-crypto-core-ristretto255-sub.md)
-   [sodium\_crypto\_scalarmult\_ristretto255()](function.sodium-crypto-scalarmult-ristretto255.md)
-   [sodium\_crypto\_scalarmult\_ristretto255\_base()](function.sodium-crypto-scalarmult-ristretto255-base.md)
