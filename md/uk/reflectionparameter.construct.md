---
navigation:
  - reflectionparameter.clone.md: '« ReflectionParameter::\_\_clone'
  - reflectionparameter.export.md: 'ReflectionParameter::export »'
  - index.md: PHP Manual
  - class.reflectionparameter.md: ReflectionParameter
title: 'ReflectionParameter::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionParameter::\_\_construct

(PHP 5, PHP 7, PHP 8)

ReflectionParameter::\_\_construct — Конструктор

### Опис

public **ReflectionParameter::\_\_construct**(string|array|object`$function`, int|string`$param`) .

Створює екземпляр [ReflectionParameter](class.reflectionparameter.md)

### Список параметрів

`function`

Функція, параметр якої потрібно відобразити.

`param`

Або ціле число (int), що вказує позицію параметра (починаючи з нуля) або ім'я параметра у вигляді рядка (string).

### Приклади

**Приклад #1 Использования класса[ReflectionParameter](class.reflectionparameter.md)**

```php
<?php
function foo($a, $b, $c) { }
function bar(Exception $a, &$b, $c) { }
function baz(ReflectionFunction $a, $b = 1, $c = null) { }
function abc() { }

$reflect = new ReflectionFunction('foo');

echo $reflect;

foreach ($reflect->getParameters() as $i => $param) {
    printf(
        "-- Аргумент #%d: %s {\n".
        "   Класс: %s\n".
        "   Допускает значения NULL: %s\n".
        "   Передаётся по ссылке: %s\n".
        "   Необязательный?: %s\n".
        "}\n",
        $i, // можно использовать $param->getPosition()
        $param->getName(),
        var_export($param->getClass(), 1),
        var_export($param->allowsNull(), 1),
        var_export($param->isPassedByReference(), 1),
        $param->isOptional() ? 'да' : 'нет'
    );
}
?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [ReflectionFunctionAbstract::getParameters()](reflectionfunctionabstract.getparameters.md) \- Отримує параметри
-   [ReflectionFunction::\_\_construct()](reflectionfunction.construct.md) \- Конструктор класу ReflectionFunction
-   [ReflectionMethod::\_\_construct()](reflectionmethod.construct.md) \- Конструктор класу ReflectionMethod
-   [Конструктори](language.oop5.decon.md#language.oop5.decon.constructor)
