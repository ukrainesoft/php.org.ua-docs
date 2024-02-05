---
navigation:
  - language.attributes.reflection.md: « Читання атрибутів за допомогою Reflection API
  - language.references.md: Пояснення посилань »
  - index.md: PHP Manual
  - language.attributes.md: Атрибути
title: Оголошення класів атрибутів
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Оголошення класів атрибутів

Хоча й немає суворої вимоги, краще виконувати рекомендацію — створювати клас для кожного атрибуту. У найпростішому випадку необхідно створити порожній клас із атрибутом `#[Attribute]`клас якого можна імпортувати з глобального простору імен через оператор use.

**Приклад #1 Простий клас з атрибутом**

```php
<?php

namespace Example;

use Attribute;

#[Attribute]
class MyAttribute
{
}
```

Щоб обмежити типи сутностей, на які можна націлити атрибут, необхідно в момент оголошення атрибута `#[Attribute]` передати як перший аргумент бітову маску.

**Приклад #2 Специфікація вказівки цілей, яким атрибут може бути наданий**

```php
<?php

namespace Example;

use Attribute;

#[Attribute(Attribute::TARGET_METHOD | Attribute::TARGET_FUNCTION)]
class MyAttribute
{
}
```

Після такого декларування спроба присвоїти атрибут **MyAttribute** іншої сутності, тип якої відрізняється від методу або функції, призведе до викидання винятку під час виклику [ReflectionAttribute::newInstance()](reflectionattribute.newinstance.md)

Можна вказати такі цілі:

-   **`Attribute::TARGET_CLASS`**
-   **`Attribute::TARGET_FUNCTION`**
-   **`Attribute::TARGET_METHOD`**
-   **`Attribute::TARGET_PROPERTY`**
-   **`Attribute::TARGET_CLASS_CONSTANT`**
-   **`Attribute::TARGET_PARAMETER`**
-   **`Attribute::TARGET_ALL`**

За умовчанням атрибут можна присвоїти сутності лише один раз. Присвоїти однакові атрибути однієї сутності можна, якщо оголосити атрибут `#[Attribute]` з прапором **`Attribute::IS_REPEATABLE`** у бітовій масці.

**Приклад #3 Застосування константи IS\_REPEATABLE при оголошенні атрибуту для дозволу його багаторазового надання**

```php
<?php

namespace Example;

use Attribute;

#[Attribute(Attribute::TARGET_METHOD | Attribute::TARGET_FUNCTION | Attribute::IS_REPEATABLE)]
class MyAttribute
{
}
```
