---
navigation:
  - phardata.setmetadata.md: '« PharData::setMetadata'
  - phardata.setstub.md: 'PharData::setStub »'
  - index.md: PHP Manual
  - class.phardata.md: PharData
title: 'PharData::setSignatureAlgorithm'
---
# PharData::setSignatureAlgorithm

(No version information available, might only be in Git)

PharData::setSignatureAlgorithm — Встановити алгоритм підписання phar-архіву та застосування його

### Опис

```methodsynopsis
public PharData::setSignatureAlgorithm(int $algo, ?string $privateKey = null): void
```

> **Зауваження**
> 
> Для коректної роботи з об'єктами [Phar](class.phar.md) цьому методу необхідне встановлення значення php.ini `phar.readonly` в `0`. В іншому випадку, буде викинуто виняток [PharException](class.pharexception.md)

Встановлює алгоритм підписання phar-архіву та застосовує його. Доступні такі алгоритми підписання: `Phar::MD5` `Phar::SHA1` `Phar::SHA256` `Phar::SHA512` і `Phar::OPENSSL`. (Pgp поки не підтримується, замість нього використовується SHA-1).

### Список параметрів

`algo`

Одна з констант: `Phar::MD5` `Phar::SHA1` `Phar::SHA256` `Phar::SHA512` або `Phar::OPENSSL`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.md) більшість помилок. Для архівів на основі zip або tar викидає виняток [BadMethodCallException](class.badmethodcallexception.md). При помилках запису на диск викидає виняток [PharException](class.pharexception.md)

### список змін

| Версия | Описание |
| --- | --- |
|  | `privateKey` тепер допускає значення null. |

### Дивіться також

-   [Phar::getSupportedSignatures()](phar.getsupportedsignatures.md) - Отримати масив підтримуваних алгоритмів підпису архіву
-   [Phar::getSignature()](phar.getsignature.md) - Отримати MD5/SHA1/SHA256/SHA512/OpenSSL підпис Phar-архіву
