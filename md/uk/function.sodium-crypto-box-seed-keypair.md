Детерміністичний висновок ключової пари з одного ключа

-   [« sodiumcryptoboxsecretkey](function.sodium-crypto-box-secretkey.html)
    
-   [sodiumcryptobox »](function.sodium-crypto-box.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Детерміністичний висновок ключової пари з одного ключа
    

# sodiumcryptoboxseedkeypair

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoboxseedkeypair - Детерміністичний висновок ключової пари з одного ключа

### Опис

```methodsynopsis
sodium_crypto_box_seed_keypair(string $seed): string
```

Скріплює початкове значення для формування секретного ключа, витягує відкритий ключ та повертає їх у вигляді пари ключів.

Функції `*_seed_keypair` ідеально підходять для створення пари ключів із паролю та солі. Використовуйте результат як `seed` для створення бажаних ключів.

### Список параметрів

`seed`

Якісь криптографічні дані. Має бути 32 байти.

### Значення, що повертаються

Ключова пара X25519 (секретний та відкритий ключі).