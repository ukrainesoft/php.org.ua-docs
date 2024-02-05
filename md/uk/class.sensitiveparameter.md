---
navigation:
  - returntypewillchange.construct.md: '« ReturnTypeWillChange::\_\_construct'
  - sensitiveparameter.construct.md: 'SensitiveParameter::\_\_construct »'
  - index.md: PHP Manual
  - reserved.attributes.md: Зумовлені атрибути
title: Клас SensitiveParameter
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SensitiveParameter

(PHP 8 >= 8.2.0)

## Вступ

Атрибутом розмічають параметр із чутливим значенням, яке буде відредаговано при попаданні у трасування стека.

## Огляд класів

```classsynopsis

    
     final
     class SensitiveParameter
     {

    /* Методы */
    
   public __construct()

   }
```

## Приклади

```php
<?php

function defaultBehavior(
    string $secret,
    string $normal
) {
    throw new Exception('Error!');
}

function sensitiveParametersWithAttribute(
    #[\SensitiveParameter]
    string $secret,
    string $normal
) {
    throw new Exception('Error!');
}

try {
    defaultBehavior('password', 'normal');
} catch (Exception $e) {
    echo $e, PHP_EOL, PHP_EOL;
}

try {
    sensitiveParametersWithAttribute('password', 'normal');
} catch (Exception $e) {
    echo $e, PHP_EOL, PHP_EOL;
}

?>
```

Результат виконання наведеного прикладу PHP 8.2 аналогічний:

```
Exception: Error! in example.php:7
Stack trace:
#0 example.php(19): defaultBehavior('password', 'normal')
#1 {main}

Exception: Error! in example.php:15
Stack trace:
#0 example.php(25): sensitiveParametersWithAttribute(Object(SensitiveParameterValue), 'normal')
#1 {main}
```

## Дивіться також

-   [Введення в атрибути](language.attributes.md)
-   [SensitiveParameterValue](class.sensitiveparametervalue.md)

## Зміст

-   [SensitiveParameter::\_\_construct](sensitiveparameter.construct.md)— Створює новий екземпляр атрибуту Sensitive Parameter
