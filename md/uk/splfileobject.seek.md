Переклад файлового покажчика на заданий рядок

-   [« SplFileObject::rewind](splfileobject.rewind.html)
    
-   [SplFileObject::setCsvControl »](splfileobject.setcsvcontrol.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileObject](class.splfileobject.html)
    
-   Переклад файлового покажчика на заданий рядок
    

# SplFileObject::seek

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::seek - Переклад файлового покажчика на заданий рядок

### Опис

```methodsynopsis
public SplFileObject::seek(int $line): void
```

Переводить файловий покажчик на заданий рядок.

### Список параметрів

`line`

Номер рядка, починаючи з 0, який потрібно перейти.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [LogicException](class.logicexception.html), якщо аргумент `line` набуває негативного значення.

### Приклади

**Приклад #1 Приклад використання **SplFileObject::seek()****

Цей приклад виводить третій рядок скрипта, що знаходиться на 2-й позиції.

```php
<?php
$file = new SplFileObject(__FILE__);
$file->seek(2);
echo $file->current();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
$file->seek(2);
```

### Дивіться також

-   [SplFileObject::current()](splfileobject.current.html) - Отримати поточний рядок файлу
-   [SplFileObject::key()](splfileobject.key.html) - Отримати номер рядка
-   [SplFileObject::next()](splfileobject.next.html) - Читати наступний рядок
-   [SplFileObject::rewind()](splfileobject.rewind.html) - Перемотування файлового покажчика на початок файлу
-   [SplFileObject::valid()](splfileobject.valid.html) - Перевіряє, чи кінець файлу (EOF) досягнуто.