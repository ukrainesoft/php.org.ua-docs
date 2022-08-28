Обрізає файл до заданої довжини

-   [« SplFileObject::ftell](splfileobject.ftell.html)
    
-   [SplFileObject::fwrite »](splfileobject.fwrite.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileObject](class.splfileobject.html)
    
-   Обрізає файл до заданої довжини
    

# SplFileObject::ftruncate

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::ftruncate — Обрізає файл до заданої довжини

### Опис

```methodsynopsis
public SplFileObject::ftruncate(int $size): bool
```

Відкидає всі дані у файлі після байта `size`

### Список параметрів

`size`

Розмір, під який потрібно підігнати файл.

> **Зауваження**
> 
> Якщо `size` більше поточного розміру файлу, в кінці будуть додані нульові байти.
> 
> Якщо `size` менше розміру файлу, зайві дані будуть втрачені.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SplFileObject::ftruncate()****

```php
<?php
// Создать файл, содержащий "Hello World!"
$file = new SplFileObject("/tmp/ftruncate", "w+");
$file->fwrite("Hello World!");

// Обрезать до 5 байт
$file->ftruncate(5);

// Перемотка к началу файла и чтение данные
$file->rewind();
echo $file->fgets();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Hello
```

### Дивіться також

-   [ftruncate()](function.ftruncate.html) - Урізує файл до вказаної довжини