Подання у вигляді рядка

-   [« ReflectionFunction::isDisabled](reflectionfunction.isdisabled.html)
    
-   [ReflectionFunctionAbstract »](class.reflectionfunctionabstract.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionFunction](class.reflectionfunction.html)
    
-   Подання у вигляді рядка
    

# ReflectionFunction::toString

(PHP 5, PHP 7, PHP 8)

ReflectionFunction::toString — Подання у вигляді рядка

### Опис

```methodsynopsis
public ReflectionFunction::__toString(): string
```

Подання у вигляді рядка.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Результат виконання схожий на висновок [ReflectionFunction::export()](reflectionfunction.export.html)

### Приклади

**Приклад #1 Приклад використання **ReflectionFunction::toString()****

```php
<?php
function title($title, $name)
{
    return sprintf("%s. %s\r\n", $title, $name);
}

echo new ReflectionFunction('title');
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Function [ <user> function title ] {
  @@ Command line code 1 - 1

  - Parameters [2] {
    Parameter #0 [ <required> $title ]
    Parameter #1 [ <required> $name ]
  }
}
```

### Дивіться також

-   [ReflectionFunction::export()](reflectionfunction.export.html) - Експортує функції
-   [toString()](language.oop5.magic.html#object.tostring)