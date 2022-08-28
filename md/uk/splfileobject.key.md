Отримати номер рядка

-   [« SplFileObject::hasChildren](splfileobject.haschildren.html)
    
-   [SplFileObject::next »](splfileobject.next.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileObject](class.splfileobject.html)
    
-   Отримати номер рядка
    

# SplFileObject::key

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::key — Отримати номер рядка

### Опис

```methodsynopsis
public SplFileObject::key(): int
```

Отримує номер поточного рядка.

> **Зауваження**
> 
> Цей номер може відрізнятись від реального положення файлового покажчика, коли читаються рядки фіксованої довжини із завданням цієї довжини методом [SplFileObject::setMaxLineLen()](splfileobject.setmaxlinelen.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає номер поточного рядка.

### Приклади

**Приклад #1 Приклад використання **SplFileObject::key()****

```php
<?php
$file = new SplFileObject("lipsum.txt");
foreach ($file as $line) {
    echo $file->key() . ". " . $line;
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
0. Lorem ipsum dolor sit amet, consectetur adipiscing elit.
1. Duis nec sapien felis, ac sodales nisl.
2. Lorem ipsum dolor sit amet, consectetur adipiscing elit.
```

**Приклад #2 Приклад використання **SplFileObject::key()** при заданні довжини рядка методом [SplFileObject::setMaxLineLen()](splfileobject.setmaxlinelen.html)**

```php
<?php
$file = new SplFileObject("lipsum.txt");
$file->setMaxLineLen(20);
foreach ($file as $line) {
    echo $file->key() . ". " . $line . "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
0. Lorem ipsum dolor s
1. it amet, consectetu
2. r adipiscing elit.
3.

4. Duis nec sapien fel
5. is, ac sodales nisl
6. .

7. Lorem ipsum dolor s
8. it amet, consectetu
9. r adipiscing elit.
```

### Дивіться також

-   [SplFileObject::current()](splfileobject.current.html) - Отримати поточний рядок файлу
-   [SplFileObject::seek()](splfileobject.seek.html) - Переклад файлового покажчика на заданий рядок
-   [SplFileObject::next()](splfileobject.next.html) - Читати наступний рядок
-   [SplFileObject::rewind()](splfileobject.rewind.html) - Перемотування файлового покажчика на початок файлу
-   [SplFileObject::valid()](splfileobject.valid.html) - Перевіряє, чи кінець файлу (EOF) досягнуто.