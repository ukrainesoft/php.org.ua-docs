---
navigation:
  - splfileobject.setcsvcontrol.md: '« SplFileObject::setCsvControl'
  - splfileobject.setmaxlinelen.md: 'SplFileObject::setMaxLineLen »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::setFlags'
---
# SplFileObject::setFlags

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::setFlags — Встановлює прапори для SplFileObject

### Опис

```methodsynopsis
public SplFileObject::setFlags(int $flags): void
```

Встановлює прапори, які будуть використовуватись [SplFileObject](class.splfileobject.md)

### Список параметрів

`flags`

Бітова маска прапори для встановлення. Дивіться [константи SplFileObject](class.splfileobject.md#splfileobject.constants) щоб отримати список доступних прапорів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **SplFileObject::setFlags()****

```php
<?php
$file = new SplFileObject("data.csv");
$file->setFlags(SplFileObject::READ_CSV);
foreach ($file as $fields) {
    var_dump($fields);
}
?>
```

### Дивіться також

-   [SplFileObject::getFlags()](splfileobject.getflags.md) - Отримує прапори налаштування об'єкта SplFileObject
