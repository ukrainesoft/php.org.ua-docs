Викликає функцію

-   [« ReflectionFunction::getClosure](reflectionfunction.getclosure.html)
    
-   [ReflectionFunction::invokeArgs »](reflectionfunction.invokeargs.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionFunction](class.reflectionfunction.html)
    
-   Викликає функцію
    

# ReflectionFunction::invoke

(PHP 5, PHP 7, PHP 8)

ReflectionFunction::invoke — Викликає функцію

### Опис

```methodsynopsis
public ReflectionFunction::invoke(mixed ...$args): mixed
```

Викликає відбиту (reflected) функцію.

### Список параметрів

`args`

Передані функції аргументи. Може приймати змінну кількість аргументів за аналогією до [call\_user\_func()](function.call-user-func.html)

### Значення, що повертаються

Повертає результат виконання викликаної функції.

### Приклади

**Приклад #1 Приклад використання **ReflectionFunction::invoke()****

```php
<?php
function title($title, $name)
{
    return sprintf("%s. %s\r\n", $title, $name);
}

$function = new ReflectionFunction('title');

echo $function->invoke('Dr', 'Phil');
?>
```

Результат виконання цього прикладу:

```
Dr. Phil
```

### Примітки

> **Зауваження**
> 
> **ReflectionFunction::invoke()** не можна використовувати, якщо очікуються параметри посилання. Замість нього слід використовувати [ReflectionFunction::invokeArgs()](reflectionfunction.invokeargs.html) (Передача посилань у списку аргументів).

### Дивіться також

-   [ReflectionFunction::export()](reflectionfunction.export.html) - Експортує функції
-   [\_\_invoke()](language.oop5.magic.html#object.invoke)
-   [call\_user\_func()](function.call-user-func.html) - Викликає callback-функцію, задану у першому параметрі