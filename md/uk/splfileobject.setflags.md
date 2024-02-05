---
navigation:
  - splfileobject.setcsvcontrol.md: '« SplFileObject::setCsvControl'
  - splfileobject.setmaxlinelen.md: 'SplFileObject::setMaxLineLen »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::setFlags'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileObject::setFlags

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

SplFileObject::setFlags — Встановлює прапори для SplFileObject

### Опис

```methodsynopsis
public SplFileObject::setFlags(int $flags): void
```

Встановлює прапори, які будуть використовуватись [SplFileObject](class.splfileobject.md)

### Список параметрів

`flags`

Битовая маска флагов для установки. Смотрите[константи SplFileObject](class.splfileobject.md#splfileobject.constants) щоб отримати список доступних прапорів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**SplFileObject::setFlags()\*\*\*\*

```php
<?php
$file = new SplFileObject("data.csv");
$file->setFlags(SplFileObject::READ_CSV);
foreach ($file as $fields) {
    var_dump($fields);
}
?>
```

### Дивіться також

-   [SplFileObject::getFlags()](splfileobject.getflags.md) \- Отримує прапори налаштування об'єкта SplFileObject
