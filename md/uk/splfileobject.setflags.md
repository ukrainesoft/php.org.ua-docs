Встановлює прапори для SplFileObject

-   [« SplFileObject::setCsvControl](splfileobject.setcsvcontrol.html)
    
-   [SplFileObject::setMaxLineLen »](splfileobject.setmaxlinelen.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileObject](class.splfileobject.html)
    
-   Встановлює прапори для SplFileObject
    

# SplFileObject::setFlags

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::setFlags — Встановлює прапори для SplFileObject

### Опис

```methodsynopsis
public SplFileObject::setFlags(int $flags): void
```

Встановлює прапори, які будуть використовуватись [SplFileObject](class.splfileobject.html)

### Список параметрів

`flags`

Бітова маска прапори для встановлення. Дивіться [константы SplFileObject](class.splfileobject.html#splfileobject.constants) щоб отримати список доступних прапорів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **SplFileObject::setFlags()****

```php
<?php
$file = new SplFileObject("data.csv");
$file->setFlags(SplFileObject::READ_CSV);
foreach ($file as $fields) {
    var_dump($fields);
}
?>
```

### Дивіться також

-   [SplFileObject::getFlags()](splfileobject.getflags.html) - Отримує прапори налаштування об'єкта SplFileObject