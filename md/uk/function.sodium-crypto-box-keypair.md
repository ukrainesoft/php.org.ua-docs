Згенерувати випадковим чином секретний ключ та відповідний йому відкритий ключ

-   [« sodiumcryptoboxkeypairfromsecretkeyandpublickey](function.sodium-crypto-box-keypair-from-secretkey-and-publickey.html)
    
-   [sodiumcryptoboxopen »](function.sodium-crypto-box-open.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Згенерувати випадковим чином секретний ключ та відповідний йому відкритий ключ
    

# sodiumcryptoboxkeypair

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoboxkeypair — Згенерувати випадковим чином секретний ключ і відповідний відкритий ключ

### Опис

```methodsynopsis
sodium_crypto_box_keypair(): string
```

Створює секретний та відкритий ключі як один рядок.

Щоб отримати секретний ключ із цього уніфікованого рядка ключової пари, дивіться [sodiumcryptoboxsecretkey()](function.sodium-crypto-box-secretkey.html). Щоб отримати відкритий ключ із цього уніфікованого рядка ключової пари, дивіться [sodiumcryptoboxpublickey()](function.sodium-crypto-box-publickey.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Один рядок містить секретний ключ X25519 і відповідний відкритий ключ X25519.