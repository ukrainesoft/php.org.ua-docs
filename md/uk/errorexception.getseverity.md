Отримує серйозність виключення

-   [« ErrorException::\_\_construct](errorexception.construct.html)
    
-   [Error »](class.error.html)
    
-   [PHP Manual](index.html)
    
-   [ErrorException](class.errorexception.html)
    
-   Отримує серйозність виключення
    

# ErrorException::getSeverity

(PHP 5> = 5.1.0, PHP 7, PHP 8)

ErrorException::getSeverity — Отримує серйозність виключення

### Опис

```methodsynopsis
final public ErrorException::getSeverity(): int
```

Повертає серйозність виключення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рівень серйозності виключення.

### Приклади

**Приклад #1 Приклад використання **ErrorException::getSeverity()****

```php
<?php
try {
    throw new ErrorException("Сообщение об исключении", 0, E_USER_ERROR);
} catch(ErrorException $e) {
    echo "Серьёзность этого исключения равна: " . $e->getSeverity();
    var_dump($e->getSeverity() === E_USER_ERROR);
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Серьёзность этого исключения равна: 256
bool(true)
```