Конструктор класу ReflectionFunction

-   [« ReflectionFunction](class.reflectionfunction.html)
    
-   [ReflectionFunction::export »](reflectionfunction.export.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionFunction](class.reflectionfunction.html)
    
-   Конструктор класу ReflectionFunction
    

# ReflectionFunction::construct

(PHP 5, PHP 7, PHP 8)

ReflectionFunction::construct - Конструктор класу ReflectionFunction

### Опис

public **ReflectionFunction::construct**[Closure](class.closure.html)|string `$function`

Створює об'єкт класу [ReflectionFunction](class.reflectionfunction.html)

### Список параметрів

`function`

Ім'я функції для відображення або [замыкание](functions.anonymous.html)

### Помилки

Об'єкт класу [ReflectionException](class.reflectionexception.html), якщо аргумент `function` не містить допустимої функції.

### Приклади

**Приклад #1 Приклад використання **ReflectionFunction::construct()****

```php
<?php
/**
 * Простой счётчик
 *
 * @return    int
 */
function counter1()
{
    static $c = 0;
    return ++$c;
}

/**
 * Другой счётчик
 *
 * @return    int
 */
$counter2 = function()
{
    static $d = 0;
    return ++$d;

};

function dumpReflectionFunction($func)
{
    // Вывод основной информации
    printf(
        "\n\n===> %s функция '%s'\n".
        "     объявлена в %s\n".
        "     строки с %d по %d\n",
        $func->isInternal() ? 'internal' : 'user-defined',
        $func->getName(),
        $func->getFileName(),
        $func->getStartLine(),
        $func->getEndline()
    );

    // Печать документации
    printf("---> Документация:\n %s\n", var_export($func->getDocComment(), 1));

    // Вывод статических переменных
    if ($statics = $func->getStaticVariables())
    {
        printf("---> Статические переменные: %s\n", var_export($statics, 1));
    }
}

// Создание объекта класса ReflectionFunction
dumpReflectionFunction(new ReflectionFunction('counter1'));
dumpReflectionFunction(new ReflectionFunction($counter2));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
===> user-defined функция 'counter1'
     объявлена в Z:\reflectcounter.php
     строки с 7 по 11
---> Документация:
 '/**
 * Простой счётчик
 *
 * @return    int
 */'
---> Статические переменные: array (
  'c' => 0,
)


===> user-defined функция '{closure}'
     объявлена в Z:\reflectcounter.php
     строки с 18 по 23
---> Документация:
 '/**
 * Другой счётчик
 *
 * @return    int
 */'
---> Статические переменные: array (
  'd' => 0,
)
```

### Дивіться також

-   [ReflectionMethod::\_\_construct()](reflectionmethod.construct.html) - Конструктор класу ReflectionMethod
-   [Конструкторы](language.oop5.decon.html#language.oop5.decon.constructor)