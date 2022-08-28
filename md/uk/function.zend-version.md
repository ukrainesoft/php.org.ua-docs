Отримує версію двигуна Zend

-   [« zend\_thread\_id](function.zend-thread-id.html)
    
-   [phpdbg »](book.phpdbg.html)
    
-   [PHP Manual](index.html)
    
-   [Опции PHP/информационные функции](ref.info.html)
    
-   Отримує версію двигуна Zend
    

# zendversion

(PHP 4, PHP 5, PHP 7, PHP 8)

zendversion — Отримує версію двигуна Zend

### Опис

```methodsynopsis
zend_version(): string
```

Повертає рядок з номером версії ядра Zend Engine, що працює в даний момент.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає номер версії Zend Engine у ​​вигляді рядка.

### Приклади

**Приклад #1 Приклад використання **zendversion()****

```php
<?php
echo "Версия движка Zend: " . zend_version();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Версия движка Zend: 2.2.0
```

### Дивіться також

-   [phpinfo()](function.phpinfo.html) - Виводить інформацію про поточну конфігурацію PHP
-   [phpcredits()](function.phpcredits.html) - Виводить список розробників PHP
-   [phpversion()](function.phpversion.html) - Отримує поточну версію PHP