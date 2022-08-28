Отримати максимальну довжину рядка

-   [« SplFileObject::getFlags](splfileobject.getflags.html)
    
-   [SplFileObject::hasChildren »](splfileobject.haschildren.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileObject](class.splfileobject.html)
    
-   Отримати максимальну довжину рядка
    

# SplFileObject::getMaxLineLen

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::getMaxLineLen — Отримати максимальну довжину рядка

### Опис

```methodsynopsis
public SplFileObject::getMaxLineLen(): int
```

Отримує максимальну довжину рядка, встановлену за допомогою [SplFileObject::setMaxLineLen()](splfileobject.setmaxlinelen.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає максимальну довжину рядка, якщо вона була встановлена ​​за допомогою [SplFileObject::setMaxLineLen()](splfileobject.setmaxlinelen.html), за замовчуванням `0`

### Приклади

**Приклад #1 Приклад використання **SplFileObject::getMaxLineLen()****

```php
<?php
$file = new SplFileObject("file.txt");
var_dump($file->getMaxLineLen());

$file->setMaxLineLen(20);
var_dump($file->getMaxLineLen());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(0)
int(20)
```

### Дивіться також

-   [SplFileObject::setMaxLineLen()](splfileobject.setmaxlinelen.html) - Встановити максимальну довжину рядка