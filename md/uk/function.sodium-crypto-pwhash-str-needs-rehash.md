Визначає, чи потрібно повторно використовувати пароль

-   [« sodium\_crypto\_pwhash\_scryptsalsa208sha256](function.sodium-crypto-pwhash-scryptsalsa208sha256.html)
    
-   [sodium\_crypto\_pwhash\_str\_verify »](function.sodium-crypto-pwhash-str-verify.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Визначає, чи потрібно повторно використовувати пароль
    

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

Налаштований opslimit; дивіться [sodium\_crypto\_pwhash\_str()](function.sodium-crypto-pwhash-str.html)

`memlimit`

Налаштований memlimit; дивіться [sodium\_crypto\_pwhash\_str()](function.sodium-crypto-pwhash-str.html)

### Значення, що повертаються

Повертає **`true`**якщо наданий memlimit/opslimit не відповідає тому, що зберігається в хеші. Повертає **`false`**якщо вони збігаються.