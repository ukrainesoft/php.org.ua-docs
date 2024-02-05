---
navigation:
  - rarentry.getname.md: '« RarEntry::getName'
  - rarentry.getstream.md: 'RarEntry::getStream »'
  - index.md: PHP Manual
  - class.rarentry.md: RarEntry
title: 'RarEntry::getPackedSize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RarEntry::getPackedSize

(PECL rar >= 0.1)

RarEntry::getPackedSize — Повертає розмір стисненого елемента

### Опис

```methodsynopsis
public RarEntry::getPackedSize(): int
```

Повертає розмір стисненого елемента архіву.

> **Зауваження** :
> 
> Врахуйте, що на платформах з 32-бітними цілими long (включаючи Windows x64), максимальний розмір, що повертається, обмежений 2 ГБ. Перевірте константу **`PHP_INT_MAX`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає розмір стисненого елемента, або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL rar 2.0.0 | Даний метод тепер повертає правильні значення для стиснутих даних більше 2 ГБ на платформах з 64 бітними цілими (int) і ніколи не повертає негативні значення на всіх платформах. |

### Приклади

**Пример #1 Пример использования**RarEntry::getPackedSize()\*\*\*\*

```php
<?php

$rar_file = rar_open('example.rar') or die("Не удалось открыть Rar архив");

$entry = rar_entry_get($rar_file, 'Dir/file.txt') or die("Не удалось найти такую запись");

echo "Размер сжатого элемента " . $entry->getName() . " = " . $entry->getPackedSize() . " байтов";

?>
```
