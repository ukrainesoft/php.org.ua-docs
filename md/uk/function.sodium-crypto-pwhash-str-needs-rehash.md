---
navigation:
  - function.sodium-crypto-pwhash-scryptsalsa208sha256.html: « sodiumcryptopwhashscryptsalsa208sha256
  - function.sodium-crypto-pwhash-str-verify.html: sodiumcryptopwhashstrverify »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptopwhashstrneedsrehash
---
# sodiumcryptopwhashstrneedsrehash

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptopwhashstrneedsrehash — Визначає, чи потрібно повторно використовувати пароль

### Опис

```methodsynopsis
sodium_crypto_pwhash_str_needs_rehash(string $password, int $opslimit, int $memlimit): bool
```

Визначає, чи потрібно повторно використовувати пароль на основі поточного хеш-значення `opslimit` і `memlimit`

### Список параметрів

`password`

Хеш пароля

`opslimit`

Налаштований opslimit; дивіться [sodiumcryptopwhashstr()](function.sodium-crypto-pwhash-str.md)

`memlimit`

Налаштований memlimit; дивіться [sodiumcryptopwhashstr()](function.sodium-crypto-pwhash-str.md)

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо наданий memlimit/opslimit не відповідає тому, що зберігається в хеші. Повертає \*\*`false`\*\*якщо вони збігаються.
