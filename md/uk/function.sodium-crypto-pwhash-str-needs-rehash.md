---
navigation:
  - function.sodium-crypto-pwhash-scryptsalsa208sha256.md: « sodium\_crypto\_pwhash\_scryptsalsa208sha256
  - function.sodium-crypto-pwhash-str-verify.md: sodium\_crypto\_pwhash\_str\_verify »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_pwhash\_str\_needs\_rehash
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_pwhash\_str\_needs\_rehash

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_pwhash\_str\_needs\_rehash — Визначає, чи потрібно повторно використовувати пароль

### Опис

```methodsynopsis
sodium_crypto_pwhash_str_needs_rehash(string $password, int $opslimit, int $memlimit): bool
```

Определяет, следует ли повторно использовать пароль, на основе текущего хеш-значения`opslimit`и`memlimit`

### Список параметрів

`password`

Хеш пароля

`opslimit`

Налаштований opslimit; дивіться [sodium\_crypto\_pwhash\_str()](function.sodium-crypto-pwhash-str.md)

`memlimit`

Налаштований memlimit; дивіться [sodium\_crypto\_pwhash\_str()](function.sodium-crypto-pwhash-str.md)

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо наданий memlimit/opslimit не відповідає тому, що зберігається в хеші. Повертає \*\*`false`\*\*якщо вони збігаються.
