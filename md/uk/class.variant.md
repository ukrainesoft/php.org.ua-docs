---
navigation:
  - dotnet.construct.html: '« dotnet::construct'
  - variant.construct.html: 'variant::construct »'
  - index.html: PHP Manual
  - book.com.html: COM
title: Клас variant
---
# Клас variant

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

## Вступ

VARIANT – це еквівалент zval для COM; це структура, яка може містити значення різних допустимих типів. Клас variant входить у модуль COM і дозволяє більше контролювати значення, що передаються від PHP до COM і назад.

## Огляд класів

```synopsis

     
    


    
     
      class variant
     
     {


    /* Методы */
    
   public __construct(mixed $value = null, int $type = VT_EMPTY, int $codepage = CP_ACP)

   }
```

## Приклади variant

**Приклад #1 Приклад використання variant**

```php
<?php
$v = new variant(42);
print "Тип — " . variant_get_type($v) . "<br/>";
print "Значение — " . $v . "<br/>";
?>
```

> **Зауваження**
> 
> Коли повертається значення або витягається властивість, variant перетворюється на значення PHP тільки якщо є прямий зв'язок між типами, що не призведе до втрати інформації. В інших випадках результат повернеться у вигляді екземпляра класу variant. Ви можете примусово вказати PHP конвертувати значення в типи PHP використовуючи оператор приведення типів або перетворювати їх у рядок, використовуючи функцію [print](function.print.html). Ви можете використовувати безліч функцій класу для арифметичних операцій без приведення значень типів PHP з ризиком втрати інформації.

Дивіться також [variantgettype()](function.variant-get-type.html)

## Зміст

-   [variant::construct](variant.construct.html) - Конструктор класу variant
