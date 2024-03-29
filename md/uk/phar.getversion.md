---
navigation:
  - phar.getsupportedsignatures.md: '« Phar::getSupportedSignatures'
  - phar.hasmetadata.md: 'Phar::hasMetadata »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::getVersion'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::getVersion

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::getVersion — Отримати версію Phar-архіву

### Опис

```methodsynopsis
public Phar::getVersion(): string
```

Повертає версію API відкритого Phar-архіву.

### Список параметрів

### Значення, що повертаються

Версія API відкритого архіву. Не переплутайте версію API завантаженого модуля phar. Кожен Phar-архів має жорстко прописану версію API, за допомогою якого його створювали у маніфесті. Детальну документацію можна прочитати на сторінці [Формат файлу Phar](phar.fileformat.md)

### Дивіться також

-   [Phar::apiVersion()](phar.apiversion.md) \- Повертає версію API
