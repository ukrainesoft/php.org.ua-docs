---
navigation:
  - phar.getsupportedsignatures.html: '« Phar::getSupportedSignatures'
  - phar.hasmetadata.html: 'Phar::hasMetadata »'
  - index.html: PHP Manual
  - class.phar.html: Phar
title: 'Phar::getVersion'
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

Версія API відкритого архіву. Не переплутайте версію API завантаженого модуля phar. Кожен Phar-архів має жорстко прописану версію API, за допомогою якого його створювали у маніфесті. Детальну документацію можна прочитати на сторінці [Формат файла Phar](phar.fileformat.md)

### Дивіться також

-   [Phar::apiVersion()](phar.apiversion.md) - Повертає версію API
