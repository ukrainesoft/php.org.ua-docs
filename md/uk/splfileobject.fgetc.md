---
navigation:
  - splfileobject.fflush.md: '« SplFileObject::fflush'
  - splfileobject.fgetcsv.md: 'SplFileObject::fgetcsv »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::fgetc'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileObject::fgetc

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

SplFileObject::fgetc — Отримує символ із файлу

### Опис

```methodsynopsis
public SplFileObject::fgetc(): string|false
```

Отримує символ із файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок, що містить один символ, прочитаний із файлу, або \*\*`false`\*\*при достижении конца файла (EOF).

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Логічний тип](language.types.boolean.md)Используйте[оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### Приклади

**Пример #1 Пример использования**SplFileObject::fgetc()\*\*\*\*

```php
<?php
$file = new SplFileObject('file.txt');
while (false !== ($char = $file->fgetc())) {
    echo "$char\n";
}
?>
```

### Дивіться також

-   [SplFileObject::fgets()](splfileobject.fgets.md) \- Отримує рядок із файлу
