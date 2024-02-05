---
navigation:
  - attribute.construct.md: '« Attribute::\_\_construct'
  - allowdynamicproperties.construct.md: 'AllowDynamicProperties::\_\_construct »'
  - index.md: PHP Manual
  - reserved.attributes.md: Зумовлені атрибути
title: Клас AllowDynamicProperties
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас AllowDynamicProperties

(PHP 8 >= 8.2.0)

## Вступ

Атрибут використовується для маркування класів, які дозволяють використовувати [динамічні властивості](language.oop5.properties.md#language.oop5.properties.dynamic-properties)

## Огляд класів

```classsynopsis

    
     final
     class AllowDynamicProperties
     {

    /* Методы */
    
   public __construct()

   }
```

## Приклади

Динамічні властивості застаріли, починаючи з PHP 8.2.0, тому їх використання без маркування класу цим атрибутом призведе до повідомлення про старіння.

```php
<?php
class DefaultBehaviour { }

#[\AllowDynamicProperties]
class ClassAllowsDynamicProperties { }

$o1 = new DefaultBehaviour();
$o2 = new ClassAllowsDynamicProperties();

$o1->nonExistingProp = true;
$o2->nonExistingProp = true;
?>
```

Результат виконання наведеного прикладу в PHP 8.2:

```
Deprecated: Creation of dynamic property DefaultBehaviour::$nonExistingProp is deprecated in file on line 10
```

## Дивіться також

[Введення в атрибути](language.attributes.md)

## Зміст

-   [AllowDynamicProperties::\_\_construct](allowdynamicproperties.construct.md)— Створює новий екземпляр атрибуту AllowDynamicProperties
