Отримати MD5/SHA1/SHA256/SHA512/OpenSSL підпис Phar-архіву

-   [« Phar::getPath](phar.getpath.html)
    
-   [Phar::getStub »](phar.getstub.html)
    
-   [PHP Manual](index.html)
    
-   [Phar](class.phar.html)
    
-   Отримати MD5/SHA1/SHA256/SHA512/OpenSSL підпис Phar-архіву
    

# Phar::getSignature

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::getSignature — Отримати MD5/SHA1/SHA256/SHA512/OpenSSL підпис Phar-архіву

### Опис

```methodsynopsis
public Phar::getSignature(): array|false
```

Повертає перевірочний підпис phar-архіву у вигляді рядка шістнадцяткових цифр.

### Список параметрів

### Значення, що повертаються

Масив, що містить цифровий підпис відкритого архіву за ключом `hash`, і `MD5` `SHA-1` `SHA-256` `SHA-512` або `OpenSSL` за ключом `hash_type`. Підпис - це хеш, обчислений від вмісту архіву, яку можна використовуватиме перевірки його цілісності. Коректний підпис потрібен для всіх phar-архівів, що запускаються, якщо дозволена INI-змінна [phar.requirehash](phar.configuration.html#ini.phar.require-hash). Якщо сигнатури немає, функція повертає **`false`**