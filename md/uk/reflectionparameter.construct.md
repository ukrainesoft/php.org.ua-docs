Конструктор

-   [« ReflectionParameter::\_\_clone](reflectionparameter.clone.html)
    
-   [ReflectionParameter::export »](reflectionparameter.export.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionParameter](class.reflectionparameter.html)
    
-   Конструктор
    

# ReflectionParameter::construct

(PHP 5, PHP 7, PHP 8)

ReflectionParameter::construct — Конструктор

### Опис

public **ReflectionParameter::construct**(string|array|object `$function`, int|string `$param`

Створює екземпляр [ReflectionParameter](class.reflectionparameter.html)

### Список параметрів

`function`

Функція, параметр якої потрібно відобразити.

`param`

Або ціле число (int), що вказує позицію параметра (починаючи з нуля) або ім'я параметра у вигляді рядка (string).

### Приклади

**Приклад #1 Використання класу [ReflectionParameter](class.reflectionparameter.html)**

```php
<?php
function foo($a, $b, $c) { }
function bar(Exception $a, &$b, $c) { }
function baz(ReflectionFunction $a, $b = 1, $c = null) { }
function abc() { }

$reflect = new ReflectionFunction('foo');

echo $reflect;

foreach ($reflect->getParameters() as $i => $param) {
    printf(
        "-- Аргумент #%d: %s {\n".
        "   Класс: %s\n".
        "   Допускает значения NULL: %s\n".
        "   Передаётся по ссылке: %s\n".
        "   Необязательный?: %s\n".
        "}\n",
        $i, // можно использовать $param->getPosition()
        $param->getName(),
        var_export($param->getClass(), 1),
        var_export($param->allowsNull(), 1),
        var_export($param->isPassedByReference(), 1),
        $param->isOptional() ? 'да' : 'нет'
    );
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Function [ <user> function foo ] {
  @@ /Users/philip/cvs/phpdoc/a 2 - 2

  - Parameters [3] {
    Parameter #0 [ <required> $a ]
    Parameter #1 [ <required> $b ]
    Parameter #2 [ <required> $c ]
  }
}
-- Аргумент #0: a {
   Класс: NULL
   Допускает значения NULL: true
   Передаётся по ссылке: false
   Необязательный?: нет
}
-- Аргумент #1: b {
   Класс: NULL
   Допускает значения NULL: true
   Передаётся по ссылке: false
   Необязательный?: нет
}
-- Аргумент #2: c {
   Класс: NULL
   Допускает значения NULL: true
   Передаётся по ссылке: false
   Необязательный?: нет
}
```

### Дивіться також

-   [ReflectionFunctionAbstract::getParameters()](reflectionfunctionabstract.getparameters.html) - Отримує параметри
-   [ReflectionFunction::\_\_construct()](reflectionfunction.construct.html) - Конструктор класу ReflectionFunction
-   [ReflectionMethod::\_\_construct()](reflectionmethod.construct.html) - Конструктор класу ReflectionMethod
-   [Конструкторы](language.oop5.decon.html#language.oop5.decon.constructor)