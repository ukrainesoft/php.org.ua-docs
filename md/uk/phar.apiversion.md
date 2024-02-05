---
navigation:
  - phar.addfromstring.md: '« Phar::addFromString'
  - phar.buildfromdirectory.md: 'Phar::buildFromDirectory »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::apiVersion'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::apiVersion

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::apiVersion — Повертає версію API

### Опис

```methodsynopsis
final public static Phar::apiVersion(): string
```

Повертає версію API формату phar-файлу, яка буде використана для створення архівів. Модуль Phar підтримує читання з версії API 1.0.0. Для використання хешів SHA-256 та SHA-512 потрібна версія API 1.1.0, а для зберігання порожніх директорій потрібна версія API 1.1.1.

### Список параметрів

### Значення, що повертаються

Рядок версії API, як у `"1.0.0"`

### Приклади

**Приклад #1 Приклад використання** Phar::apiVersion()\*\*\*\*

```php
<?php
echo Phar::apiVersion();
?>
```

Результат виконання наведеного прикладу:

```
1.1.1
```
