---
navigation:
  - class.reflectionclass.md: « ReflectionClass
  - reflectionclass.export.md: 'ReflectionClass::export »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::\_\_construct

(PHP 5, PHP 7, PHP 8)

ReflectionClass::\_\_construct — Створює об'єкт класу ReflectionClass

### Опис

public **ReflectionClass::\_\_construct**(object|string`$objectOrClass`) .

Створює новий об'єкт класу [ReflectionClass](class.reflectionclass.md)

### Список параметрів

`objectOrClass`

Як аргумент може приймати рядок (string), що містить ім'я класу, що досліджується, або об'єкт (object).

### Помилки

Викликає виняток [ReflectionException](class.reflectionexception.md)якщо заданий клас не існує.

### Приклади

**Приклад #1 Простий приклад використання ReflectionClass**

```php
<?php
$reflection = new ReflectionClass('Exception');
echo $reflection;
?>
```

Висновок наведеного прикладу буде схожим на:

```
Class [ <internal:Core> class Exception implements Stringable, Throwable ] {

  - Constants [0] {
  }

  - Static properties [0] {
  }

  - Static methods [0] {
  }

  - Properties [7] {
    Property [ protected $message = '' ]
    Property [ private string $string = '' ]
    Property [ protected $code = 0 ]
    Property [ protected string $file = '' ]
    Property [ protected int $line = 0 ]
    Property [ private array $trace = [] ]
    Property [ private ?Throwable $previous = NULL ]
  }

  - Methods [11] {
    Method [ <internal:Core> private method __clone ] {

      - Parameters [0] {
      }
      - Return [ void ]
    }

    Method [ <internal:Core, ctor> public method __construct ] {

      - Parameters [3] {
        Parameter #0 [ <optional> string $message = "" ]
        Parameter #1 [ <optional> int $code = 0 ]
        Parameter #2 [ <optional> ?Throwable $previous = null ]
      }
    }

    Method [ <internal:Core> public method __wakeup ] {

      - Parameters [0] {
      }
      - Tentative return [ void ]
    }

    Method [ <internal:Core, prototype Throwable> final public method getMessage ] {

      - Parameters [0] {
      }
      - Return [ string ]
    }

    Method [ <internal:Core, prototype Throwable> final public method getCode ] {

      - Parameters [0] {
      }
    }

    Method [ <internal:Core, prototype Throwable> final public method getFile ] {

      - Parameters [0] {
      }
      - Return [ string ]
    }

    Method [ <internal:Core, prototype Throwable> final public method getLine ] {

      - Parameters [0] {
      }
      - Return [ int ]
    }

    Method [ <internal:Core, prototype Throwable> final public method getTrace ] {

      - Parameters [0] {
      }
      - Return [ array ]
    }

    Method [ <internal:Core, prototype Throwable> final public method getPrevious ] {

      - Parameters [0] {
      }
      - Return [ ?Throwable ]
    }

    Method [ <internal:Core, prototype Throwable> final public method getTraceAsString ] {

      - Parameters [0] {
      }
      - Return [ string ]
    }

    Method [ <internal:Core, prototype Stringable> public method __toString ] {

      - Parameters [0] {
      }
      - Return [ string ]
    }
  }
}
```

### Дивіться також

-   [ReflectionObject::\_\_construct()](reflectionobject.construct.md) \- Конструктор класу ReflectionObject
-   [Конструктори](language.oop5.decon.md#language.oop5.decon.constructor)
