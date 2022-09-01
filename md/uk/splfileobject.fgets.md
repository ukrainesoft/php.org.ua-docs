---
navigation:
  - splfileobject.fgetcsv.md: '« SplFileObject::fgetcsv'
  - splfileobject.fgetss.md: 'SplFileObject::fgetss »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::fgets'
---
# SplFileObject::fgets

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::fgets — Отримує рядок із файлу

### Опис

```methodsynopsis
public SplFileObject::fgets(): string
```

Отримує рядок із файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок, що містить наступний рядок із файлу, або **`false`** у разі виникнення помилки.

### Помилки

Викидає [RuntimeException](class.runtimeexception.md)якщо файл не може бути прочитаний.

### Приклади

**Приклад #1 Приклад використання **SplFileObject::fgets()****

Цей приклад построчно виводить вміст `file.txt`

```php
<?php
$file = new SplFileObject("file.txt");
while (!$file->eof()) {
    echo $file->fgets();
}
?>
```

### Дивіться також

-   [fgets()](function.fgets.md) - Читає рядок із файлу
-   [SplFileObject::fgetss()](splfileobject.fgetss.md) - Отримати рядок із файлу та видалити теги HTML
-   [SplFileObject::fgetc()](splfileobject.fgetc.md) - Отримує символ із файлу
-   [SplFileObject::current()](splfileobject.current.md) - Отримати поточний рядок файлу
