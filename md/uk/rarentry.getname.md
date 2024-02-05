---
navigation:
  - rarentry.getmethod.md: '« RarEntry::getMethod'
  - rarentry.getpackedsize.md: 'RarEntry::getPackedSize »'
  - index.md: PHP Manual
  - class.rarentry.md: RarEntry
title: 'RarEntry::getName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RarEntry::getName

(PECL rar >= 0.1)

RarEntry::getName — Повертає ім'я елемента

### Опис

```methodsynopsis
public RarEntry::getName(): string
```

Повертає ім'я елемента масиву (разом із шляхом).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я елемента у вигляді рядка, або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL rar 2.0.0 | Починаючи з версії 2.0.0, повертається рядок у кодуванні Unicode/UTF-8. |

### Приклади

**Пример #1 Пример использования**RarEntry::getName()\*\*\*\*

```php
<?php

// этот пример работает, даже если страница не в кодировке UTF-8
// для перекодирования в UTF-8 вызывается mb_convert_encoding

$rar_file = rar_open('example.rar') or die("Не удалось открыть Rar архив");

$entry = rar_entry_get($rar_file, 'Dir/file.txt') or die("Не удалось найти такую запись");

echo "Имя элемента: " . mb_convert_encoding(
    htmlentities(
        $entry->getName(),
        ENT_COMPAT,
        "UTF-8"
    ),
    "HTML-ENTITIES",
    "UTF-8"
);

?>
```
