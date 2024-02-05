---
navigation:
  - allowdynamicproperties.construct.md: '« AllowDynamicProperties::\_\_construct'
  - override.construct.md: 'Override::\_\_construct »'
  - index.md: PHP Manual
  - reserved.attributes.md: Зумовлені атрибути
title: Клас Override
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Override

(PHP 8 >= 8.3.0)

## Вступ

## Огляд класів

```classsynopsis

    
     final
     class Override
     {

    /* Методы */
    
   public __construct()

   }
```

## Приклади

```php
<?php

class Base {
    protected function foo(): void {}
}

final class Extended extends Base {
    #[\Override]
    protected function boo(): void {}
}

?>
```

Результат виконання наведеного прикладу PHP 8.3 аналогічний:

```
Fatal error: Extended::boo() has #[\Override] attribute, but no matching parent method exists
```

## Дивіться також

-   [Атрибути](language.attributes.md)

## Зміст

-   [Override::\_\_construct](override.construct.md)— Створює новий екземпляр атрибуту Override
