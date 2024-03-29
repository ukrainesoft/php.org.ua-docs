---
navigation:
  - reflection.examples.md: « Приклади
  - class.reflection.md: Reflection »
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Розширення
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Розширення

Якщо вам потрібна спеціалізована версія вбудованого класу (який, наприклад, зможе генерувати кольоровий HTML при експорті, матиме легкодоступні властивості замість методів або якісь допоміжні методи), то можете просто взяти і розширити його.

**Приклад #1 Розширення вбудованих класів**

```php
<?php
/**
 * Мой класс Reflection_Method
 */
class My_Reflection_Method extends ReflectionMethod
{
    public $visibility = array();

    public function __construct($o, $m)
    {
        parent::__construct($o, $m);
        $this->visibility = Reflection::getModifierNames($this->getModifiers());
    }
}

/**
 * Демо-класс #1
 *
 */
class T {
    protected function x() {}
}

/**
 * Демо-класс #2
 *
 */
class U extends T {
    function x() {}
}

// Выведем информацию о методе
var_dump(new My_Reflection_Method('U', 'x'));
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(My_Reflection_Method)#1 (3) {
  ["visibility"]=>
  array(1) {
    [0]=>
    string(6) "public"
  }
  ["name"]=>
  string(1) "x"
  ["class"]=>
  string(1) "U"
}
```

**Застереження**

Коли ви перевизначаєте конструктор, не забудьте обов'язково викликати батьківський конструктор до будь-якого доданого коду. Якщо так не робити, ви можете отримати повідомлення про помилку виду: `Fatal error: Internal error: Failed to retrieve the reflection object`
