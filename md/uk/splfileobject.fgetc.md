Отримує символ із файлу

-   [« SplFileObject::fflush](splfileobject.fflush.html)
    
-   [SplFileObject::fgetcsv »](splfileobject.fgetcsv.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileObject](class.splfileobject.html)
    
-   Отримує символ із файлу
    

# SplFileObject::fgetc

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::fgetc — Отримує символ із файлу

### Опис

```methodsynopsis
public SplFileObject::fgetc(): string|false
```

Отримує символ із файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок, що містить один символ, прочитаний із файлу, або **`false`** при досягненні кінця файлу (EOF).

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Булев тип](language.types.boolean.html). Використовуйте [оператор ===](language.operators.comparison.html) для перевірки значення, яке повертається цією функцією.

### Приклади

**Приклад #1 Приклад використання **SplFileObject::fgetc()****

```php
<?php
$file = new SplFileObject('file.txt');
while (false !== ($char = $file->fgetc())) {
    echo "$char\n";
}
?>
```

### Дивіться також

-   [SplFileObject::fgets()](splfileobject.fgets.html) - Отримує рядок із файлу