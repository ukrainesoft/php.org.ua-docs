---
navigation:
  - splfileobject.ftell.md: '« SplFileObject::ftell'
  - splfileobject.fwrite.md: 'SplFileObject::fwrite »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::ftruncate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileObject::ftruncate

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

SplFileObject::ftruncate — Обрізає файл до заданої довжини

### Опис

```methodsynopsis
public SplFileObject::ftruncate(int $size): bool
```

Відкидає всі дані у файлі після байта `size`

### Список параметрів

`size`

Розмір, під який потрібно підігнати файл.

> **Зауваження** :
> 
> Якщо `size` більше поточного розміру файлу, в кінці будуть додані нульові байти.
> 
> Якщо `size` менше розміру файлу, зайві дані будуть втрачені.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** SplFileObject::ftruncate()\*\*\*\*

```php
<?php
// Создать файл, содержащий "Hello World!"
$file = new SplFileObject("/tmp/ftruncate", "w+");
$file->fwrite("Hello World!");

// Обрезать до 5 байт
$file->ftruncate(5);

// Перемотка к началу файла и чтение данные
$file->rewind();
echo $file->fgets();
?>
```

Висновок наведеного прикладу буде схожим на:

```
Hello
```

### Дивіться також

-   [ftruncate()](function.ftruncate.md) \- Урізує файл до вказаної довжини
