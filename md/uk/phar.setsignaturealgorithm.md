---
navigation:
  - phar.setmetadata.md: '« Phar::setMetadata'
  - phar.setstub.md: 'Phar::setStub »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::setSignatureAlgorithm'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::setSignatureAlgorithm

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.1.0)

Phar::setSignatureAlgorithm — Встановити алгоритм підписання phar-архіву та застосування його

### Опис

```methodsynopsis
public Phar::setSignatureAlgorithm(int $algo, ?string $privateKey = null): void
```

> **Зауваження** :
> 
> Для коректної роботи з об'єктами [Phar](class.phar.md) цьому методу необхідне встановлення значення php.ini `phar.readonly`в . В іншому випадку, буде викинуто виняток [PharException](class.pharexception.md)

Встановлює алгоритм підписання phar-архіву та застосовує його. Доступні такі алгоритми підписання: `Phar::MD5` `Phar::SHA1` `Phar::SHA256` `Phar::SHA512`и`Phar::OPENSSL`

Зверніть увагу, що для всіх phar-архівів, що виконуються, підпис створюється автоматично, з використанням за умовчанням `SHA1`. Архіви з даними на основі tar або zip (створені за допомогою класу [PharData](class.phardata.md)) повинні мати явно створену за допомогою **Phar::setSignatureAlgorithm()** підпис.

### Список параметрів

`algo`

Одна из констант:`Phar::MD5` `Phar::SHA1` `Phar::SHA256` `Phar::SHA512`или`Phar::OPENSSL`

`privateKey`

Секретний ключ OpenSSL, витягнутий із сертифіката, або файл із ключем OpenSSL:

```php
<?php
$private = openssl_get_privatekey(file_get_contents('private.pem'));
$pkey = '';
openssl_pkey_export($private, $pkey);
$p->setSignatureAlgorithm(Phar::OPENSSL, $pkey);
?>
```

Подробиці про іменування та розміщення файлу відкритого ключа дивіться у розділі [Введення в phar](phar.using.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.md) за будь-яких помилок, крім помилок запису на диск. При помилках запису на диск викидає виняток [PharException](class.pharexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `privateKey` тепер допускає значення null. |

### Дивіться також

-   [Phar::getSupportedSignatures()](phar.getsupportedsignatures.md) \- Отримати масив підтримуваних алгоритмів підпису архіву
-   [Phar::getSignature()](phar.getsignature.md) \- Отримати MD5/SHA1/SHA256/SHA512/OpenSSL підпис Phar-архіву
