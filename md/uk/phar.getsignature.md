---
navigation:
  - phar.getpath.md: '« Phar::getPath'
  - phar.getstub.md: 'Phar::getStub »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::getSignature'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Масив, що містить цифровий підпис відкритого архіву за ключом `hash`, и`MD5` `SHA-1` `SHA-256` `SHA-512`или`OpenSSL`по ключу`hash_type`. Підпис - це хеш, обчислений від вмісту архіву, яку можна використовуватиме перевірки його цілісності. Коректний підпис потрібен для всіх архівів, що запускаються, якщо дозволена INI-змінна [phar.require\_hash](phar.configuration.md#ini.phar.require-hash). Якщо сигнатури немає, функція повертає **`false`**
